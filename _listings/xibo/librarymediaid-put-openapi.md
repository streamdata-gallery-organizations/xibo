---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Edit Media
  description: Edit a Media Item in the Library
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /campaign:
    get:
      summary: Search Campaigns
      description: Search all Campaigns this user has access to
      operationId: campaignSearch
      x-api-path-slug: campaign-get
      parameters:
      - in: formData
        name: campaignId
        description: Filter by Campaign Id
      - in: formData
        name: hasLayouts
        description: Filter by has layouts
      - in: formData
        name: isLayoutSpecific
        description: Filter by whether this Campaign is specific to a Layout or User
          added
      - in: formData
        name: name
        description: Filter by Name
      - in: formData
        name: retired
        description: Filter by retired
      - in: formData
        name: tags
        description: Filter by Tags
      - in: formData
        name: totalDuration
        description: Should we total the duration?
      responses:
        200:
          description: OK
      tags:
      - Search
      - Campaigns
    post:
      summary: Add Campaign
      description: Add a Campaign
      operationId: campaignAdd
      x-api-path-slug: campaign-post
      parameters:
      - in: formData
        name: name
        description: Name for this Campaign
      responses:
        200:
          description: OK
      tags:
      - Campaign
  /campaign/{campaignId}:
    put:
      summary: Edit Campaign
      description: Edit an existing Campaign
      operationId: campaignEdit
      x-api-path-slug: campaigncampaignid-put
      parameters:
      - in: path
        name: campaignId
        description: The Campaign ID to Edit
      - in: formData
        name: name
        description: Name for this Campaign
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Campaign
    delete:
      summary: Delete Campaign
      description: Delete an existing Campaign
      operationId: campaignDelete
      x-api-path-slug: campaigncampaignid-delete
      parameters:
      - in: path
        name: campaignId
        description: The Campaign ID to Delete
      responses:
        200:
          description: OK
      tags:
      - Campaign
  /campaign/layout/assign/{campaignId}:
    post:
      summary: Assign Layouts
      description: Assign Layouts to a Campaign
      operationId: campaignAssignLayout
      x-api-path-slug: campaignlayoutassigncampaignid-post
      parameters:
      - in: path
        name: campaignId
        description: The Campaign ID
      - in: formData
        name: layoutId
        description: Array of Layout ID/Display Orders to Assign
      - in: formData
        name: unassignLayoutId
        description: Array of Layout ID/Display Orders to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Layouts
  /clock:
    get:
      summary: The current CMS time
      description: The Time
      operationId: clock
      x-api-path-slug: clock-get
      responses:
        200:
          description: OK
      tags:
      - The
      - Current
      - CMS
      - Time
  /command:
    get:
      summary: Command Search
      description: Search this users Commands
      operationId: commandSearch
      x-api-path-slug: command-get
      parameters:
      - in: formData
        name: code
        description: Filter by Command Code
      - in: formData
        name: command
        description: Filter by Command Name
      - in: formData
        name: commandId
        description: Filter by Command Id
      responses:
        200:
          description: OK
      tags:
      - Command
      - Search
    post:
      summary: Command Add
      description: Add a Command
      operationId: commandAdd
      x-api-path-slug: command-post
      parameters:
      - in: formData
        name: code
        description: A unique code for this command
      - in: formData
        name: command
        description: The Command Name
      - in: formData
        name: description
        description: A description for the command
      responses:
        200:
          description: OK
      tags:
      - Command
  /command/{commandId}:
    put:
      summary: Edit Command
      description: Edit the provided command
      operationId: commandEdit
      x-api-path-slug: commandcommandid-put
      parameters:
      - in: formData
        name: command
        description: The Command Name
      - in: path
        name: commandId
        description: The Command Id to Edit
      - in: formData
        name: description
        description: A description for the command
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Command
    delete:
      summary: Delete Command
      description: Delete the provided command
      operationId: commandDelete
      x-api-path-slug: commandcommandid-delete
      parameters:
      - in: path
        name: commandId
        description: The Command Id to Delete
      responses:
        200:
          description: OK
      tags:
      - Command
  /dataset:
    get:
      summary: DataSet Search
      description: Search this users DataSets
      operationId: dataSetSearch
      x-api-path-slug: dataset-get
      parameters:
      - in: formData
        name: code
        description: Filter by DataSet Code
      - in: formData
        name: dataSet
        description: Filter by DataSet Name
      - in: formData
        name: dataSetId
        description: Filter by DataSet Id
      - in: formData
        name: embed
        description: Embed related data such as columns
      responses:
        200:
          description: OK
      tags:
      - DataSet
      - Search
    post:
      summary: Add DataSet
      description: Add a DataSet
      operationId: dataSetAdd
      x-api-path-slug: dataset-post
      parameters:
      - in: formData
        name: authentication
        description: HTTP Authentication method None|Basic|Digest
      - in: formData
        name: clearRate
        description: How often in seconds should this remote DataSet be truncated
      - in: formData
        name: code
        description: A code for this DataSet
      - in: formData
        name: dataRoot
        description: The root of the data in the Remote source which is used as the
          base for all remote columns
      - in: formData
        name: dataSet
        description: The DataSet Name
      - in: formData
        name: description
        description: A description of this DataSet
      - in: formData
        name: isRemote
        description: Is this a remote DataSet?
      - in: formData
        name: method
        description: The Request Method GET or POST
      - in: formData
        name: password
        description: HTTP Authentication Password
      - in: formData
        name: postData
        description: query parameter encoded data to add to the request
      - in: formData
        name: refreshRate
        description: How often in seconds should this remote DataSet be refreshed
      - in: formData
        name: runsAfter
        description: An optional dataSetId which should be run before this Remote
          DataSet
      - in: formData
        name: summarize
        description: Should the data be aggregated? None|Summarize|Count
      - in: formData
        name: summarizeField
        description: Which field should be used to summarize
      - in: formData
        name: uri
        description: The URI, without query parameters
      - in: formData
        name: username
        description: HTTP Authentication User Name
      responses:
        200:
          description: OK
      tags:
      - DataSet
  /dataset/{dataSetId}:
    put:
      summary: Edit DataSet
      description: Edit a DataSet
      operationId: dataSetEdit
      x-api-path-slug: datasetdatasetid-put
      parameters:
      - in: formData
        name: authentication
        description: HTTP Authentication method None|Basic|Digest
      - in: formData
        name: clearRate
        description: How often in seconds should this remote DataSet be truncated
      - in: formData
        name: code
        description: A code for this DataSet
      - in: formData
        name: dataRoot
        description: The root of the data in the Remote source which is used as the
          base for all remote columns
      - in: formData
        name: dataSet
        description: The DataSet Name
      - in: path
        name: dataSetId
        description: The DataSet ID
      - in: formData
        name: description
        description: A description of this DataSet
      - in: formData
        name: isRemote
        description: Is this a remote DataSet?
      - in: formData
        name: method
        description: The Request Method GET or POST
      - in: formData
        name: password
        description: HTTP Authentication Password
      - in: formData
        name: postData
        description: query parameter encoded data to add to the request
      - in: formData
        name: refreshRate
        description: How often in seconds should this remote DataSet be refreshed
      - in: formData
        name: runsAfter
        description: An optional dataSetId which should be run before this Remote
          DataSet
      - in: formData
        name: summarize
        description: Should the data be aggregated? None|Summarize|Count
      - in: formData
        name: summarizeField
        description: Which field should be used to summarize
      - in: formData
        name: uri
        description: The URI, without query parameters
      - in: formData
        name: username
        description: HTTP Authentication User Name
      responses:
        200:
          description: OK
      tags:
      - Edit
      - DataSet
    delete:
      summary: Delete DataSet
      description: Delete a DataSet
      operationId: dataSetDelete
      x-api-path-slug: datasetdatasetid-delete
      parameters:
      - in: path
        name: dataSetId
        description: The DataSet ID
      responses:
        200:
          description: OK
      tags:
      - DataSet
  /dataset/copy/{dataSetId}:
    post:
      summary: Copy DataSet
      description: Copy a DataSet
      operationId: dataSetCopy
      x-api-path-slug: datasetcopydatasetid-post
      parameters:
      - in: formData
        name: code
        description: A code for this DataSet
      - in: formData
        name: dataSet
        description: The DataSet Name
      - in: path
        name: dataSetId
        description: The DataSet ID
      - in: formData
        name: description
        description: A description of this DataSet
      responses:
        200:
          description: OK
      tags:
      - Copy
      - DataSet
  /dataset/import/{dataSetId}:
    post:
      summary: Import CSV
      description: Import a CSV into a DataSet
      operationId: dataSetImport
      x-api-path-slug: datasetimportdatasetid-post
      parameters:
      - in: formData
        name: csvImport_{dataSetColumnId}
        description: You need to provide dataSetColumnId after csvImport_, to know
          your dataSet columns Ids, you will need to use the GET /dataset/{dataSetId}/column
          call first
      - in: path
        name: dataSetId
        description: The DataSet ID to import into
      - in: formData
        name: files
        description: The file
      - in: formData
        name: ignorefirstrow
        description: flag (0,1), Set to 1 to Ignore first row, useful if the CSV file
          has headings
      - in: formData
        name: overwrite
        description: flag (0,1) Set to 1 to erase all content in the dataSet and overwrite
          it with new content in this import
      responses:
        200:
          description: OK
      tags:
      - Import
      - CSV
  /dataset/importjson/{dataSetId}:
    post:
      summary: Import JSON
      description: Import JSON into a DataSet
      operationId: dataSetImportJson
      x-api-path-slug: datasetimportjsondatasetid-post
      parameters:
      - in: body
        name: data
        description: The row data, field name vs field data format
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: dataSetId
        description: The DataSet ID to import into
      responses:
        200:
          description: OK
      tags:
      - Import
      - JSON
  /dataset/{dataSetId}/column:
    get:
      summary: Search Columns
      description: Search Columns for DataSet
      operationId: dataSetColumnSearch
      x-api-path-slug: datasetdatasetidcolumn-get
      parameters:
      - in: formData
        name: dataSetColumnId
        description: Filter by DataSet ColumnID
      - in: path
        name: dataSetId
        description: The DataSet ID
      responses:
        200:
          description: OK
      tags:
      - Search
      - Columns
    post:
      summary: Add Column
      description: Add a Column to a DataSet
      operationId: dataSetColumnAdd
      x-api-path-slug: datasetdatasetidcolumn-post
      parameters:
      - in: formData
        name: columnOrder
        description: The display order for this column
      - in: formData
        name: dataSetColumnTypeId
        description: The column type for this column
      - in: path
        name: dataSetId
        description: The DataSet ID
      - in: formData
        name: dataTypeId
        description: The data type ID for this column
      - in: formData
        name: formula
        description: MySQL SELECT syntax formula for this Column if the column type
          is formula
      - in: formData
        name: heading
        description: The heading for the Column
      - in: formData
        name: listContent
        description: A comma separated list of content for drop downs
      - in: formData
        name: remoteField
        description: JSON-String to select Data from the Remote DataSet
      - in: formData
        name: showFilter
        description: Flag indicating whether this column should present a filter on
          DataEntry
      - in: formData
        name: showSort
        description: Flag indicating whether this column should allow sorting on DataEntry
      responses:
        200:
          description: OK
      tags:
      - Column
  /dataset/{dataSetId}/column/{dataSetColumnId}:
    put:
      summary: Edit Column
      description: Edit a Column to a DataSet
      operationId: dataSetColumnEdit
      x-api-path-slug: datasetdatasetidcolumndatasetcolumnid-put
      parameters:
      - in: formData
        name: columnOrder
        description: The display order for this column
      - in: path
        name: dataSetColumnId
        description: The Column ID
      - in: formData
        name: dataSetColumnTypeId
        description: The column type for this column
      - in: path
        name: dataSetId
        description: The DataSet ID
      - in: formData
        name: dataTypeId
        description: The data type ID for this column
      - in: formData
        name: formula
        description: MySQL SELECT syntax formula for this Column if the column type
          is formula
      - in: formData
        name: heading
        description: The heading for the Column
      - in: formData
        name: listContent
        description: A comma separated list of content for drop downs
      - in: formData
        name: remoteField
        description: JSON-String to select Data from the Remote DataSet
      - in: formData
        name: showFilter
        description: Flag indicating whether this column should present a filter on
          DataEntry
      - in: formData
        name: showSort
        description: Flag indicating whether this column should allow sorting on DataEntry
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Column
    delete:
      summary: Delete Column
      description: Delete DataSet Column
      operationId: dataSetColumnDelete
      x-api-path-slug: datasetdatasetidcolumndatasetcolumnid-delete
      parameters:
      - in: path
        name: dataSetColumnId
        description: The Column ID
      - in: path
        name: dataSetId
        description: The DataSet ID
      responses:
        200:
          description: OK
      tags:
      - Column
  /dataset/data/{dataSetId}:
    get:
      summary: DataSet Data
      description: Get Data for DataSet
      operationId: dataSetData
      x-api-path-slug: datasetdatadatasetid-get
      parameters:
      - in: path
        name: dataSetId
        description: The DataSet ID
      responses:
        200:
          description: OK
      tags:
      - DataSet
      - Data
    post:
      summary: Add Row
      description: Add a row of Data to a DataSet
      operationId: dataSetDataAdd
      x-api-path-slug: datasetdatadatasetid-post
      parameters:
      - in: formData
        name: dataSetColumnId_ID
        description: Parameter for each dataSetColumnId in the DataSet
      - in: path
        name: dataSetId
        description: The DataSet ID
      responses:
        200:
          description: OK
      tags:
      - Row
  /dataset/data/{dataSetId}/{rowId}:
    put:
      summary: Edit Row
      description: Edit a row of Data to a DataSet
      operationId: dataSetDataEdit
      x-api-path-slug: datasetdatadatasetidrowid-put
      parameters:
      - in: formData
        name: dataSetColumnId_ID
        description: Parameter for each dataSetColumnId in the DataSet
      - in: path
        name: dataSetId
        description: The DataSet ID
      - in: path
        name: rowId
        description: The Row ID of the Data to Edit
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Row
    delete:
      summary: Delete Row
      description: Delete a row of Data to a DataSet
      operationId: dataSetDataDelete
      x-api-path-slug: datasetdatadatasetidrowid-delete
      parameters:
      - in: path
        name: dataSetId
        description: The DataSet ID
      - in: path
        name: rowId
        description: The Row ID of the Data to Delete
      responses:
        200:
          description: OK
      tags:
      - Row
  /daypart:
    get:
      summary: Daypart Search
      description: Search dayparts
      operationId: dayPartSearch
      x-api-path-slug: daypart-get
      parameters:
      - in: formData
        name: dayPartId
        description: The dayPart ID to Search
      - in: formData
        name: embed
        description: Embed related data such as exceptions
      - in: formData
        name: name
        description: The name of the dayPart to Search
      responses:
        200:
          description: OK
      tags:
      - Daypart
      - Search
    post:
      summary: Daypart Add
      description: Add a Daypart
      operationId: dayPartAdd
      x-api-path-slug: daypart-post
      parameters:
      - in: formData
        name: description
        description: A description for the dayPart
      - in: formData
        name: endTime
        description: The end time for this day part
      - in: formData
        name: exceptionDays
        description: String array of exception days
      - in: formData
        name: exceptionEndTimes
        description: String array of exception end times to match the exception days
      - in: formData
        name: exceptionStartTimes
        description: String array of exception start times to match the exception
          days
      - in: formData
        name: name
        description: The Daypart Name
      - in: formData
        name: startTime
        description: The start time for this day part
      responses:
        200:
          description: OK
      tags:
      - Daypart
  /daypart/{dayPartId}:
    put:
      summary: Daypart Add
      description: Add a Daypart
      operationId: dayPartAdd
      x-api-path-slug: daypartdaypartid-put
      parameters:
      - in: path
        name: dayPartId
        description: The Daypart Id
      - in: formData
        name: description
        description: A description for the dayPart
      - in: formData
        name: endTime
        description: The end time for this day part
      - in: formData
        name: exceptionDays
        description: String array of exception days
      - in: formData
        name: exceptionEndTimes
        description: String array of exception end times to match the exception days
      - in: formData
        name: exceptionStartTimes
        description: String array of exception start times to match the exception
          days
      - in: formData
        name: name
        description: The Daypart Name
      - in: formData
        name: startTime
        description: The start time for this day part
      responses:
        200:
          description: OK
      tags:
      - Daypart
    delete:
      summary: Delete DayPart
      description: Delete the provided dayPart
      operationId: dayPartDelete
      x-api-path-slug: daypartdaypartid-delete
      parameters:
      - in: path
        name: dayPartId
        description: The Daypart Id to Delete
      responses:
        200:
          description: OK
      tags:
      - DayPart
  /display:
    get:
      summary: Display Search
      description: Search Displays for this User
      operationId: displaySearch
      x-api-path-slug: display-get
      parameters:
      - in: formData
        name: authorised
        description: Filter by authorised flag
      - in: formData
        name: clientVersion
        description: Filter by Client Version
      - in: formData
        name: display
        description: Filter by Display Name
      - in: formData
        name: displayGroupId
        description: Filter by DisplayGroup Id
      - in: formData
        name: displayId
        description: Filter by Display Id
      - in: formData
        name: displayProfileId
        description: Filter by Display Profile
      - in: formData
        name: embed
        description: Embed related data, namely displaygroups
      - in: formData
        name: hardwareKey
        description: Filter by Hardware Key
      - in: formData
        name: macAddress
        description: Filter by Mac Address
      responses:
        200:
          description: OK
      tags:
      - Display
      - Search
  /display/{displayId}:
    put:
      summary: Display Edit
      description: Edit a Display
      operationId: displayEdit
      x-api-path-slug: displaydisplayid-put
      parameters:
      - in: formData
        name: alertTimeout
        description: How long in seconds should this display wait before alerting
          when it hasnt connected
      - in: formData
        name: auditingUntil
        description: A date this Display records auditing information until
      - in: formData
        name: broadCastAddress
        description: The BroadCast Address for this Display - used by Wake On LAN
      - in: formData
        name: cidr
        description: The CIDR configuration for this Display
      - in: formData
        name: clearCachedData
        description: Clear all Cached data for this display
      - in: formData
        name: defaultLayoutId
        description: A Layout ID representing the Default Layout for this Display
      - in: formData
        name: description
        description: A description of the Display
      - in: formData
        name: display
        description: The Display Name
      - in: path
        name: displayId
        description: The Display ID
      - in: formData
        name: displayProfileId
        description: The Display Settings Profile ID
      - in: formData
        name: emailAlert
        description: Flag indicating whether the Display generates up/down email alerts
      - in: formData
        name: incSchedule
        description: Flag indicating whether the Default Layout should be included
          in the Schedule
      - in: formData
        name: latitude
        description: The Latitude of this Display
      - in: formData
        name: license
        description: The hardwareKey to use as the licence key for this Display
      - in: formData
        name: licensed
        description: Flag indicating whether this display is licensed
      - in: formData
        name: longitude
        description: The Longitude of this Display
      - in: formData
        name: rekeyXmr
        description: Clear the cached XMR configuration and send a rekey
      - in: formData
        name: secureOn
        description: The secure on configuration for this Display
      - in: formData
        name: tags
        description: A comma separated list of tags for this item
      - in: formData
        name: timeZone
        description: The timezone for this display, or empty to use the CMS timezone
      - in: formData
        name: wakeOnLanEnabled
        description: Flag indicating if Wake On LAN is enabled for this Display
      - in: formData
        name: wakeOnLanTime
        description: A h:i string representing the time that the Display should receive
          its Wake on LAN command
      responses:
        200:
          description: OK
      tags:
      - Display
      - Edit
    delete:
      summary: Display Delete
      description: Delete a Display
      operationId: displayDelete
      x-api-path-slug: displaydisplayid-delete
      parameters:
      - in: path
        name: displayId
        description: The Display ID
      responses:
        200:
          description: OK
      tags:
      - Display
  /display/requestscreenshot/{displayId}:
    put:
      summary: Request Screen Shot
      description: Notify the display that the CMS would like a screen shot to be
        sent.
      operationId: displayRequestScreenshot
      x-api-path-slug: displayrequestscreenshotdisplayid-put
      parameters:
      - in: path
        name: displayId
        description: The Display ID
      responses:
        200:
          description: OK
      tags:
      - Request
      - Screen
      - Shot
  /display/wol/{displayId}:
    post:
      summary: Issue WOL
      description: Send a Wake On LAN packet to this Display
      operationId: displayWakeOnLan
      x-api-path-slug: displaywoldisplayid-post
      parameters:
      - in: path
        name: displayId
        description: The Display ID
      responses:
        200:
          description: OK
      tags:
      - Issue
      - WOL
  /display/authorise/{displayId}:
    post:
      summary: Toggle authorised
      description: Toggle authorised for the Display.
      operationId: displayToggleAuthorise
      x-api-path-slug: displayauthorisedisplayid-post
      parameters:
      - in: path
        name: displayId
        description: The Display ID
      responses:
        200:
          description: OK
      tags:
      - Toggle
      - Authorised
  /display/defaultlayout/{displayId}:
    post:
      summary: Set Default Layout
      description: Sent the default Layout on this Display
      operationId: displayDefaultLayout
      x-api-path-slug: displaydefaultlayoutdisplayid-post
      parameters:
      - in: path
        name: displayId
        description: The Display ID
      - in: formData
        name: layoutId
        description: The Layout ID
      responses:
        200:
          description: OK
      tags:
      - Set
      - Default
      - Layout
  /displaygroup:
    get:
      summary: Get Display Groups
      description: ""
      operationId: displayGroupSearch
      x-api-path-slug: displaygroup-get
      parameters:
      - in: formData
        name: displayGroup
        description: Filter by DisplayGroup Name
      - in: formData
        name: displayGroupId
        description: Filter by DisplayGroup Id
      - in: formData
        name: displayId
        description: Filter by DisplayGroups containing a specific display
      - in: formData
        name: dynamicCriteria
        description: Filter by DisplayGroups containing a specific dynamic criteria
      - in: formData
        name: forSchedule
        description: Should the list be refined for only those groups the User can
          Schedule against?
      - in: formData
        name: isDisplaySpecific
        description: Filter by whether the Display Group belongs to a Display or is
          user created
      - in: formData
        name: nestedDisplayId
        description: Filter by DisplayGroups containing a specific display in there
          nesting
      responses:
        200:
          description: OK
      tags:
      - Display
      - Groups
    post:
      summary: Add a Display Group
      description: Add a new Display Group to the CMS
      operationId: displayGroupAdd
      x-api-path-slug: displaygroup-post
      parameters:
      - in: formData
        name: description
        description: The Display Group Description
      - in: formData
        name: displayGroup
        description: The Display Group Name
      - in: formData
        name: dynamicContent
        description: The filter criteria for this dynamic group
      - in: formData
        name: isDynamic
        description: Flag indicating whether this DisplayGroup is Dynamic
      - in: formData
        name: tags
        description: A comma separated list of tags for this item
      responses:
        200:
          description: OK
      tags:
      - Display
      - Group
  /displaygroup/{displayGroupId}:
    put:
      summary: Edit a Display Group
      description: Edit an existing Display Group identified by its Id
      operationId: displayGroupEdit
      x-api-path-slug: displaygroupdisplaygroupid-put
      parameters:
      - in: formData
        name: description
        description: The Display Group Description
      - in: formData
        name: displayGroup
        description: The Display Group Name
      - in: path
        name: displayGroupId
        description: The displayGroupId to edit
      - in: formData
        name: dynamicCriteria
        description: The filter criteria for this dynamic group
      - in: formData
        name: isDynamic
        description: Flag indicating whether this DisplayGroup is Dynamic
      - in: formData
        name: tags
        description: A comma separated list of tags for this item
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Display
      - Group
    delete:
      summary: Delete a Display Group
      description: Delete an existing Display Group identified by its Id
      operationId: displayGroupDelete
      x-api-path-slug: displaygroupdisplaygroupid-delete
      parameters:
      - in: path
        name: displayGroupId
        description: The displayGroupId to delete
      responses:
        200:
          description: OK
      tags:
      - Display
      - Group
  /displaygroup/{displayGroupId}/display/assign:
    post:
      summary: Assign one or more Displays to a Display Group
      description: Adds the provided Displays to the Display Group
      operationId: displayGroupDisplayAssign
      x-api-path-slug: displaygroupdisplaygroupiddisplayassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: displayId
        description: The Display Ids to assign
      - in: formData
        name: unassignDisplayId
        description: An optional array of Display IDs to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Displays
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/display/unassign:
    post:
      summary: Unassigns one or more Displays to a Display Group
      description: Removes the provided Displays from the Display Group
      operationId: displayGroupDisplayUnassign
      x-api-path-slug: displaygroupdisplaygroupiddisplayunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: displayId
        description: The Display Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassigns
      - More
      - Displays
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/displayGroup/assign:
    post:
      summary: Assign one or more DisplayGroups to a Display Group
      description: Adds the provided DisplayGroups to the Display Group
      operationId: displayGroupDisplayGroupAssign
      x-api-path-slug: displaygroupdisplaygroupiddisplaygroupassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: displayGroupId
        description: The displayGroup Ids to assign
      - in: formData
        name: unassignDisplayGroupId
        description: An optional array of displayGroup IDs to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - DisplayGroups
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/displayGroup/unassign:
    post:
      summary: Unassigns one or more DisplayGroups to a Display Group
      description: Removes the provided DisplayGroups from the Display Group
      operationId: displayGroupDisplayGroupUnassign
      x-api-path-slug: displaygroupdisplaygroupiddisplaygroupunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: displayGroupId
        description: The DisplayGroup Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassigns
      - More
      - DisplayGroups
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/media/assign:
    post:
      summary: Assign one or more Media items to a Display Group
      description: Adds the provided Media to the Display Group
      operationId: displayGroupMediaAssign
      x-api-path-slug: displaygroupdisplaygroupidmediaassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: mediaId
        description: The Media Ids to assign
      - in: formData
        name: unassignMediaId
        description: Optional array of Media Id to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Media
      - Items
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/media/unassign:
    post:
      summary: Unassign one or more Media items from a Display Group
      description: Removes the provided from the Display Group
      operationId: displayGroupMediaUnassign
      x-api-path-slug: displaygroupdisplaygroupidmediaunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: mediaId
        description: The Media Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassign
      - More
      - Media
      - Items
      - From
      - Display
      - Group
  /displaygroup/{displayGroupId}/layout/assign:
    post:
      summary: Assign one or more Layouts items to a Display Group
      description: Adds the provided Layouts to the Display Group
      operationId: displayGroupLayoutsAssign
      x-api-path-slug: displaygroupdisplaygroupidlayoutassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: layoutId
        description: The Layouts Ids to assign
      - in: formData
        name: unassignLayoutId
        description: Optional array of Layouts Id to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Layouts
      - Items
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/layout/unassign:
    post:
      summary: Unassign one or more Layout items from a Display Group
      description: Removes the provided from the Display Group
      operationId: displayGroupLayoutUnassign
      x-api-path-slug: displaygroupdisplaygroupidlayoutunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: layoutId
        description: The Layout Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassign
      - More
      - Layout
      - Items
      - From
      - Display
      - Group
  /displaygroup/{displayGroupId}/version:
    post:
      summary: Set the Version for this Display
      description: Sets the version instructions on all Displays in the Group
      operationId: displayGroupDisplayVersion
      x-api-path-slug: displaygroupdisplaygroupidversion-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group ID
      - in: formData
        name: mediaId
        description: The Media Id of the Installer File
      responses:
        200:
          description: OK
      tags:
      - Set
      - Versionthis
      - Display
  /displaygroup/{displayGroupId}/action/collectNow:
    post:
      summary: 'Action: Collect Now'
      description: Send the collect now action to this DisplayGroup
      operationId: displayGroupActionCollectNow
      x-api-path-slug: displaygroupdisplaygroupidactioncollectnow-post
      parameters:
      - in: path
        name: displayGroupId
        description: The display group id
      responses:
        200:
          description: OK
      tags:
      - 'Action:'
      - Collect
      - Now
  /displaygroup/{displayGroupId}/action/clearStatsAndLogs:
    post:
      summary: 'Action: Clear Stats and Logs'
      description: Clear all stats and logs on this Group
      operationId: displayGroupActionClearStatsAndLogs
      x-api-path-slug: displaygroupdisplaygroupidactionclearstatsandlogs-post
      parameters:
      - in: path
        name: displayGroupId
        description: The display group id
      responses:
        200:
          description: OK
      tags:
      - 'Action:'
      - Clear
      - Stats
      - Logs
  /displaygroup/{displayGroupId}/action/changeLayout:
    post:
      summary: 'Action: Change Layout'
      description: Send the change layout action to this DisplayGroup
      operationId: displayGroupActionChangeLayout
      x-api-path-slug: displaygroupdisplaygroupidactionchangelayout-post
      parameters:
      - in: formData
        name: changeMode
        description: Whether to queue or replace with this action
      - in: path
        name: displayGroupId
        description: The Display Group Id
      - in: formData
        name: downloadRequired
        description: Flag indicating whether the player should perform a collect before
          playing the Layout
      - in: formData
        name: duration
        description: The duration in seconds for this Layout change to remain in effect
      - in: formData
        name: layoutId
        description: The Layout Id
      responses:
        200:
          description: OK
      tags:
      - 'Action:'
      - Change
      - Layout
  /displaygroup/{displayGroupId}/action/revertToSchedule:
    post:
      summary: 'Action: Revert to Schedule'
      description: Send the revert to schedule action to this DisplayGroup
      operationId: displayGroupActionRevertToSchedule
      x-api-path-slug: displaygroupdisplaygroupidactionreverttoschedule-post
      parameters:
      - in: path
        name: displayGroupId
        description: The display group id
      responses:
        200:
          description: OK
      tags:
      - 'Action:'
      - Revert
      - To
      - Schedule
  /displaygroup/{displayGroupId}/action/overlayLayout:
    post:
      summary: 'Action: Overlay Layout'
      description: Send the overlay layout action to this DisplayGroup
      operationId: displayGroupActionOverlayLayout
      x-api-path-slug: displaygroupdisplaygroupidactionoverlaylayout-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group Id
      - in: formData
        name: downloadRequired
        description: Flag indicating whether the player should perform a collect before
          adding the Overlay
      - in: formData
        name: duration
        description: The duration in seconds for this Overlay to remain in effect
      - in: formData
        name: layoutId
        description: The Layout Id
      responses:
        200:
          description: OK
      tags:
      - 'Action:'
      - Overlay
      - Layout
  /displaygroup/{displayGroupId}/action/command:
    post:
      summary: Send Command
      description: Send a predefined command to this Group of Displays
      operationId: displayGroupActionCommand
      x-api-path-slug: displaygroupdisplaygroupidactioncommand-post
      parameters:
      - in: formData
        name: commandId
        description: The Command Id
      - in: path
        name: displayGroupId
        description: The display group id
      responses:
        200:
          description: OK
      tags:
      - Send
      - Command
  /displayprofile:
    get:
      summary: Display Profile Search
      description: Search this users Display Profiles
      operationId: displayProfileSearch
      x-api-path-slug: displayprofile-get
      parameters:
      - in: formData
        name: displayProfile
        description: Filter by DisplayProfile Name
      - in: formData
        name: displayProfileId
        description: Filter by DisplayProfile Id
      - in: formData
        name: type
        description: Filter by DisplayProfile Type (windows|android)
      responses:
        200:
          description: OK
      tags:
      - Display
      - Profile
      - Search
    post:
      summary: Add Display Profile
      description: Add a Display Profile
      operationId: displayProfileAdd
      x-api-path-slug: displayprofile-post
      parameters:
      - in: formData
        name: isDefault
        description: Flag indicating if this is the default profile for the client
          type
      - in: formData
        name: name
        description: The Name of the Display Profile
      - in: formData
        name: type
        description: The Client Type this Profile will apply to
      responses:
        200:
          description: OK
      tags:
      - Display
      - Profile
  /displayprofile/{displayProfileId}:
    put:
      summary: Edit Display Profile
      description: Edit a Display Profile
      operationId: displayProfileEdit
      x-api-path-slug: displayprofiledisplayprofileid-put
      parameters:
      - in: path
        name: displayProfileId
        description: The Display Profile ID
      - in: formData
        name: isDefault
        description: Flag indicating if this is the default profile for the client
          type
      - in: formData
        name: name
        description: The Name of the Display Profile
      - in: formData
        name: type
        description: The Client Type this Profile will apply to
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Display
      - Profile
    delete:
      summary: Delete Display Profile
      description: Delete an existing Display Profile
      operationId: displayProfileDelete
      x-api-path-slug: displayprofiledisplayprofileid-delete
      parameters:
      - in: path
        name: displayProfileId
        description: The Display Profile ID
      responses:
        200:
          description: OK
      tags:
      - Display
      - Profile
  /layout:
    get:
      summary: Search Layouts
      description: Search for Layouts viewable by this user
      operationId: layoutSearch
      x-api-path-slug: layout-get
      parameters:
      - in: formData
        name: embed
        description: Embed related data such as regions, playlists, tags, etc
      - in: formData
        name: exactTags
        description: A flag indicating whether to treat the tags filter as an exact
          match
      - in: formData
        name: layout
        description: Filter by partial Layout name
      - in: formData
        name: layoutId
        description: Filter by Layout Id
      - in: formData
        name: ownerUserGroupId
        description: Filter by users in this UserGroupId
      - in: formData
        name: retired
        description: Filter by retired flag
      - in: formData
        name: tags
        description: Filter by Tags
      - in: formData
        name: userId
        description: Filter by user Id
      responses:
        200:
          description: OK
      tags:
      - Search
      - Layouts
    post:
      summary: Add a Layout
      description: Add a new Layout to the CMS
      operationId: layoutAdd
      x-api-path-slug: layout-post
      parameters:
      - in: formData
        name: description
        description: The layout description
      - in: formData
        name: layoutId
        description: If the Layout should be created with a Template, provide the
          ID, otherwise dont provide
      - in: formData
        name: name
        description: The layout name
      - in: formData
        name: resolutionId
        description: If a Template is not provided, provide the resolutionId for this
          Layout
      responses:
        200:
          description: OK
      tags:
      - Layout
  /layout/{layoutId}:
    put:
      summary: Edit Layout
      description: Edit a Layout
      operationId: layoutEdit
      x-api-path-slug: layoutlayoutid-put
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this Layout
      - in: formData
        name: backgroundImageId
        description: A media ID to use as the background image for this Layout
      - in: formData
        name: backgroundzIndex
        description: The Layer Number to use for the background
      - in: formData
        name: description
        description: The Layout Description
      - in: path
        name: layoutId
      - in: formData
        name: name
        description: The Layout Name
      - in: formData
        name: resolutionId
        description: The Resolution ID to use on this Layout
      - in: formData
        name: retired
        description: A flag indicating whether this Layout is retired
      - in: formData
        name: tags
        description: A comma separated list of Tags
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Layout
    delete:
      summary: Delete Layout
      description: Delete a Layout
      operationId: layoutDelete
      x-api-path-slug: layoutlayoutid-delete
      parameters:
      - in: path
        name: layoutId
        description: The Layout ID to Delete
      responses:
        200:
          description: OK
      tags:
      - Layout
  /layout/retire/{layoutId}:
    put:
      summary: Retire Layout
      description: Retire a Layout so that it isn't available to Schedule. Existing
        Layouts will still be played
      operationId: layoutRetire
      x-api-path-slug: layoutretirelayoutid-put
      parameters:
      - in: path
        name: layoutId
        description: The Layout ID
      responses:
        200:
          description: OK
      tags:
      - Retire
      - Layout
  /layout/copy/{layoutId}:
    post:
      summary: Copy Layout
      description: Copy a Layout, providing a new name if applicable
      operationId: layoutCopy
      x-api-path-slug: layoutcopylayoutid-post
      parameters:
      - in: formData
        name: copyMediaFiles
        description: Flag indicating whether to make new Copies of all Media Files
          assigned to the Layout being Copied
      - in: formData
        name: description
        description: The Description for the new Layout
      - in: path
        name: layoutId
        description: The Layout ID to Copy
      - in: formData
        name: name
        description: The name for the new Layout
      responses:
        200:
          description: OK
      tags:
      - Copy
      - Layout
  /layout/{layoutId}/tag:
    post:
      summary: Tag Layout
      description: Tag a Layout with one or more tags
      operationId: layoutTag
      x-api-path-slug: layoutlayoutidtag-post
      parameters:
      - in: path
        name: layoutId
        description: The Layout Id to Tag
      - in: formData
        name: tag
        description: An array of tags
      responses:
        200:
          description: OK
      tags:
      - Tag
      - Layout
  /layout/{layoutId}/untag:
    post:
      summary: Untag Layout
      description: Untag a Layout with one or more tags
      operationId: layoutUntag
      x-api-path-slug: layoutlayoutiduntag-post
      parameters:
      - in: path
        name: layoutId
        description: The Layout Id to Untag
      - in: formData
        name: tag
        description: An array of tags
      responses:
        200:
          description: OK
      tags:
      - Untag
      - Layout
  /layout/status/{layoutId}:
    get:
      summary: Layout Status
      description: Calculate the Layout status and return a Layout
      operationId: layoutStatus
      x-api-path-slug: layoutstatuslayoutid-get
      parameters:
      - in: path
        name: layoutId
        description: The Layout Id to get the status
      responses:
        200:
          description: OK
      tags:
      - Layout
      - Status
  /library:
    get:
      summary: Library Search
      description: Search the Library for this user
      operationId: librarySearch
      x-api-path-slug: library-get
      parameters:
      - in: formData
        name: duration
        description: Filter by Duration - a number or less-than,greater-than,less-than-equal
          or great-than-equal followed by a | followed by a number
      - in: formData
        name: exactTags
        description: A flag indicating whether to treat the tags filter as an exact
          match
      - in: formData
        name: fileSize
        description: Filter by File Size - a number or less-than,greater-than,less-than-equal
          or great-than-equal followed by a | followed by a number
      - in: formData
        name: media
        description: Filter by Media Name
      - in: formData
        name: mediaId
        description: Filter by Media Id
      - in: formData
        name: ownerId
        description: Filter by Owner Id
      - in: formData
        name: ownerUserGroupId
        description: Filter by users in this UserGroupId
      - in: formData
        name: retired
        description: Filter by Retired
      - in: formData
        name: tags
        description: Filter by Tags - comma seperated
      - in: formData
        name: type
        description: Filter by Media Type
      responses:
        200:
          description: OK
      tags:
      - Library
      - Search
    post:
      summary: Add Media
      description: Add Media to the Library
      operationId: libraryAdd
      x-api-path-slug: library-post
      parameters:
      - in: formData
        name: deleteOldRevisions
        description: Flag (0 , 1), to either remove or leave the old file revisions
          (use with oldMediaId)
      - in: formData
        name: files
        description: The Uploaded File
      - in: formData
        name: name
        description: Optional Media Name
      - in: formData
        name: oldMediaId
        description: Id of an existing media file which should be replaced with the
          new upload
      - in: formData
        name: updateInLayouts
        description: Flag (0, 1), set to 1 to update this media in all layouts (use
          with oldMediaId)
      responses:
        200:
          description: OK
      tags:
      - Media
  /library/{mediaId}:
    put:
      summary: Edit Media
      description: Edit a Media Item in the Library
      operationId: libraryEdit
      x-api-path-slug: librarymediaid-put
      parameters:
      - in: formData
        name: duration
        description: The duration in seconds for this Media Item
      - in: path
        name: mediaId
        description: The Media ID to Edit
      - in: formData
        name: name
        description: Media Item Name
      - in: formData
        name: retired
        description: Flag indicating if this media is retired
      - in: formData
        name: tags
        description: Comma separated list of Tags
      - in: formData
        name: updateInLayouts
        description: Flag indicating whether to update the duration in all Layouts
          the Media is assigned to
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Media
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---