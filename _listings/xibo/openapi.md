---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 1
info:
  title: Xibo API
  description: xibo-cms-api
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
    delete:
      summary: Delete Media
      description: Delete Media from the Library
      operationId: libraryDelete
      x-api-path-slug: librarymediaid-delete
      parameters:
      - in: formData
        name: forceDelete
        description: If the media item has been used should it be force removed from
          items that uses it?
      - in: path
        name: mediaId
        description: The Media ID to Delete
      responses:
        200:
          description: OK
      tags:
      - Media
  /library/tidy:
    delete:
      summary: Tidy Library
      description: Routine tidy of the library, removing unused files.
      operationId: libraryTidy
      x-api-path-slug: librarytidy-delete
      parameters:
      - in: formData
        name: tidyGenericFiles
        description: Also delete generic files?
      responses:
        200:
          description: OK
      tags:
      - Tidy
      - Library
  /library/download/{mediaId}/{type}:
    get:
      summary: Download Media
      description: Download a Media file from the Library
      operationId: libraryDownload
      x-api-path-slug: librarydownloadmediaidtype-get
      parameters:
      - in: path
        name: mediaId
        description: The Media ID to Download
      - in: path
        name: type
        description: The Module Type of the Download
      responses:
        200:
          description: OK
      tags:
      - Download
      - Media
  /library/{mediaId}/tag:
    post:
      summary: Tag Media
      description: Tag a Media with one or more tags
      operationId: mediaTag
      x-api-path-slug: librarymediaidtag-post
      parameters:
      - in: path
        name: mediaId
        description: The Media Id to Tag
      - in: formData
        name: tag
        description: An array of tags
      responses:
        200:
          description: OK
      tags:
      - Tag
      - Media
  /library/{mediaId}/untag:
    post:
      summary: Untag Media
      description: Untag a Media with one or more tags
      operationId: mediaUntag
      x-api-path-slug: librarymediaiduntag-post
      parameters:
      - in: path
        name: mediaId
        description: The Media Id to Untag
      - in: formData
        name: tag
        description: An array of tags
      responses:
        200:
          description: OK
      tags:
      - Untag
      - Media
  /library/usage/{mediaId}:
    get:
      summary: Get Library Item Usage Report
      description: Get the records for the library item usage report
      operationId: libraryUsageReport
      x-api-path-slug: libraryusagemediaid-get
      responses:
        200:
          description: OK
      tags:
      - Library
      - Item
      - Usage
      - Report
  /library/usage/layouts/{mediaId}:
    get:
      summary: Get Library Item Usage Report for Layouts
      description: Get the records for the library item usage report for Layouts
      operationId: libraryUsageLayoutsReport
      x-api-path-slug: libraryusagelayoutsmediaid-get
      responses:
        200:
          description: OK
      tags:
      - Library
      - Item
      - Usage
      - ReportLayouts
  /about:
    get:
      summary: About
      description: Information about this API, such as Version code, etc
      operationId: about
      x-api-path-slug: about-get
      responses:
        200:
          description: OK
      tags:
      - About
  /playlist/widget/{widgetId}:
    put:
      summary: Edit a Widget
      description: Edit a Widget, please refer to individual widget Add documentation
        for module specific parameters
      operationId: WidgetEdit
      x-api-path-slug: playlistwidgetwidgetid-put
      parameters:
      - in: path
        name: widgetId
        description: The widget ID to edit
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Widget
    delete:
      summary: Delete a Widget
      description: Deleted a specified widget
      operationId: WidgetDelete
      x-api-path-slug: playlistwidgetwidgetid-delete
      parameters:
      - in: path
        name: widgetId
        description: The widget ID to delete
      responses:
        200:
          description: OK
      tags:
      - Widget
  /playlist/widget/transition/{type}/{widgetId}:
    put:
      summary: Adds In/Out transition
      description: Adds In/Out transition to a specified widget
      operationId: WidgetEditTransition
      x-api-path-slug: playlistwidgettransitiontypewidgetid-put
      parameters:
      - in: formData
        name: transitionDirection
        description: The direction for this transition, only appropriate for transitions
          that move, such as fly
      - in: formData
        name: transitionDuration
        description: Duration of this transition in milliseconds
      - in: formData
        name: transitionType
        description: 'Type of a transition, available Options: fly, fadeIn, fadeOut'
      - in: path
        name: type
        description: 'Transition type, available options: in, out'
      - in: path
        name: widgetId
        description: The widget ID to add the transition to
      responses:
        200:
          description: OK
      tags:
      - S
      - In
      - Out
      - Transition
  /playlist/widget/{widgetId}/audio:
    put:
      summary: Parameters for edting/adding audio file to a specific widget
      description: Parameters for edting/adding audio file to a specific widget
      operationId: WidgetAssignedAudioEdit
      x-api-path-slug: playlistwidgetwidgetidaudio-put
      parameters:
      - in: formData
        name: loop
        description: Flag (0, 1) Should the audio loop if it finishes before the widget
          has finished?
      - in: formData
        name: mediaId
        description: Id of a audio file in CMS library you wish to add to a widget
      - in: formData
        name: volume
        description: Volume percentage(0-100) for this audio to play at
      - in: path
        name: widgetId
        description: Id of a widget to which you want to add audio or edit existing
          audio
      responses:
        200:
          description: OK
      tags:
      - Parametersedting
      - Adding
      - Audio
      - File
      - To
      - Specific
      - Widget
    delete:
      summary: Delete assigned audio widget
      description: Delete assigned audio widget from specified widget ID
      operationId: WidgetAudioDelete
      x-api-path-slug: playlistwidgetwidgetidaudio-delete
      parameters:
      - in: path
        name: widgetId
        description: Id of a widget from which you want to delete the audio from
      responses:
        200:
          description: OK
      tags:
      - Assigned
      - Audio
      - Widget
  /notification:
    get:
      summary: Notification Search
      description: Search this users Notifications
      operationId: notificationSearch
      x-api-path-slug: notification-get
      parameters:
      - in: formData
        name: notificationId
        description: Filter by Notification Id
      - in: formData
        name: subject
        description: Filter by Subject
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Search
    post:
      summary: Notification Add
      description: Add a Notification
      operationId: notificationAdd
      x-api-path-slug: notification-post
      parameters:
      - in: formData
        name: body
        description: The Body
      - in: formData
        name: displayGroupIds
        description: The display group ids to assign this notification to
      - in: formData
        name: isEmail
        description: Flag indicating whether this notification should be emailed
      - in: formData
        name: isInterrupt
        description: Flag indication whether this notification should interrupt the
          web portal nativation/login
      - in: formData
        name: releaseDt
        description: ISO date representing the release date for this notification
      - in: formData
        name: subject
        description: The Subject
      - in: formData
        name: userGroupIds
        description: The user group ids to assign to this notification
      responses:
        200:
          description: OK
      tags:
      - Notification
  /notification/{notificationId}:
    put:
      summary: Notification Edit
      description: Edit a Notification
      operationId: notificationEdit
      x-api-path-slug: notificationnotificationid-put
      parameters:
      - in: formData
        name: body
        description: The Body
      - in: formData
        name: displayGroupIds
        description: The display group ids to assign this notification to
      - in: formData
        name: isEmail
        description: Flag indicating whether this notification should be emailed
      - in: formData
        name: isInterrupt
        description: Flag indication whether this notification should interrupt the
          web portal nativation/login
      - in: path
        name: notificationId
        description: The NotificationId
      - in: formData
        name: releaseDt
        description: ISO date representing the release date for this notification
      - in: formData
        name: subject
        description: The Subject
      - in: formData
        name: userGroupIds
        description: The user group ids to assign to this notification
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Edit
    delete:
      summary: Delete Notification
      description: Delete the provided notification
      operationId: notificationDelete
      x-api-path-slug: notificationnotificationid-delete
      parameters:
      - in: path
        name: notificationId
        description: The Notification Id to Delete
      responses:
        200:
          description: OK
      tags:
      - Notification
  /playlist/widget:
    get:
      summary: Playlist Widget Search
      description: Search widgets on a Playlist
      operationId: playlistSearch
      x-api-path-slug: playlistwidget-get
      parameters:
      - in: formData
        name: playlistId
        description: The Playlist ID to Search
      - in: formData
        name: widgetId
        description: The widget ID to Search
      responses:
        200:
          description: OK
      tags:
      - Playlist
      - Widget
      - Search
  /playlist/library/assign/{playlistId}:
    post:
      summary: Assign Library Items
      description: Assign Media from the Library to this Playlist
      operationId: playlistLibraryAssign
      x-api-path-slug: playlistlibraryassignplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Optional duration for all Media in this assignment to use on
          the Widget
      - in: formData
        name: media
        description: Array of Media IDs to assign
      - in: path
        name: playlistId
        description: The Playlist ID to assign to
      - in: formData
        name: useDuration
        description: Optional flag indicating whether to enable the useDuration field
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Library
      - Items
  /playlist/order/{playlistId}:
    post:
      summary: Order Widgets
      description: Set the order of widgets in the Playlist
      operationId: playlistOrder
      x-api-path-slug: playlistorderplaylistid-post
      parameters:
      - in: path
        name: playlistId
        description: The Playlist ID to Order
      - in: formData
        name: widgets
        description: Array of widgetIds and positions - all widgetIds present in the
          playlist need to be passed in the call with their positions
      responses:
        200:
          description: OK
      tags:
      - Order
      - Widgets
  /region/{id}:
    put:
      summary: Edit Region
      description: Edit Region
      operationId: regionEdit
      x-api-path-slug: regionid-put
      parameters:
      - in: formData
        name: height
        description: The Height
      - in: path
        name: id
        description: The Region ID to Edit
      - in: formData
        name: left
        description: The Left Coordinate
      - in: formData
        name: loop
        description: Flag indicating whether this region should loop if there is only
          1 media item in the timeline
      - in: formData
        name: top
        description: The Top Coordinate
      - in: formData
        name: transitionDirection
        description: The transition direction if required by the transition type
      - in: formData
        name: transitionDuration
        description: The transition duration in milliseconds if required by the transition
          type
      - in: formData
        name: transitionType
        description: The Transition Type
      - in: formData
        name: width
        description: The Width, default 250
      - in: formData
        name: zIndex
        description: The Layer for this Region
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Region
    post:
      summary: Add Region
      description: Add a Region to a Layout
      operationId: regionAdd
      x-api-path-slug: regionid-post
      parameters:
      - in: formData
        name: height
        description: The Height
      - in: path
        name: id
        description: The Layout ID to add the Region to
      - in: formData
        name: left
        description: The Left Coordinate
      - in: formData
        name: top
        description: The Top Coordinate
      - in: formData
        name: width
        description: The Width, default 250
      responses:
        200:
          description: OK
      tags:
      - Region
  /region/{regionId}:
    delete:
      summary: Region Delete
      description: Delete an existing region
      operationId: regionDelete
      x-api-path-slug: regionregionid-delete
      parameters:
      - in: path
        name: regionId
        description: The Region ID to Delete
      responses:
        200:
          description: OK
      tags:
      - Region
  /region/position/all/{layoutId}:
    put:
      summary: Position Regions
      description: Position all regions for a Layout
      operationId: regionPositionAll
      x-api-path-slug: regionpositionalllayoutid-put
      parameters:
      - in: path
        name: layoutId
        description: The Layout ID
      - in: formData
        name: regions
        description: Array of regions and their new positions
      responses:
        200:
          description: OK
      tags:
      - Position
      - Regions
  /resolution:
    get:
      summary: Resolution Search
      description: Search Resolutions this user has access to
      operationId: resolutionSearch
      x-api-path-slug: resolution-get
      parameters:
      - in: formData
        name: enabled
        description: Filter by Enabled
      - in: formData
        name: resolution
        description: Filter by Resolution Name
      - in: formData
        name: resolutionId
        description: Filter by Resolution Id
      responses:
        200:
          description: OK
      tags:
      - Resolution
      - Search
    post:
      summary: Add Resolution
      description: Add new Resolution
      operationId: resolutionAdd
      x-api-path-slug: resolution-post
      parameters:
      - in: formData
        name: height
        description: The Display Height of the Resolution
      - in: formData
        name: resolution
        description: A name for the Resolution
      - in: formData
        name: width
        description: The Display Width of the Resolution
      responses:
        200:
          description: OK
      tags:
      - Resolution
  /resolution/{resolutionId}:
    put:
      summary: Edit Resolution
      description: Edit new Resolution
      operationId: resolutionEdit
      x-api-path-slug: resolutionresolutionid-put
      parameters:
      - in: formData
        name: height
        description: The Display Height of the Resolution
      - in: formData
        name: resolution
        description: A name for the Resolution
      - in: path
        name: resolutionId
        description: The Resolution ID to Edit
      - in: formData
        name: width
        description: The Display Width of the Resolution
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Resolution
    delete:
      summary: Delete Resolution
      description: Delete Resolution
      operationId: resolutionDelete
      x-api-path-slug: resolutionresolutionid-delete
      parameters:
      - in: path
        name: resolutionId
        description: The Resolution ID to Delete
      responses:
        200:
          description: OK
      tags:
      - Resolution
  /schedule/data/events:
    get:
      summary: Generates the calendar that we draw events on
      description: ""
      operationId: scheduleCalendarData
      x-api-path-slug: scheduledataevents-get
      parameters:
      - in: formData
        name: displayGroupIds
        description: The DisplayGroupIds to return the schedule for
      - in: formData
        name: from
        description: From Date Timestamp in Microseconds
      - in: formData
        name: to
        description: To Date Timestamp in Microseconds
      responses:
        200:
          description: OK
      tags:
      - Generates
      - Calendar
      - That
      - We
      - Draw
      - Events
      - "On"
  /schedule/{displayGroupId}/events:
    get:
      summary: Event List
      description: ""
      operationId: scheduleCalendarData
      x-api-path-slug: scheduledisplaygroupidevents-get
      parameters:
      - in: formData
        name: date
        description: Date in Y-m-d H:i:s
      - in: path
        name: displayGroupId
        description: The DisplayGroupId to return the event list for
      responses:
        200:
          description: OK
      tags:
      - Event
      - List
  /schedule:
    post:
      summary: Add Schedule Event
      description: Add a new scheduled event for a Campaign/Layout to be shown on
        a Display Group/Display.
      operationId: scheduleAdd
      x-api-path-slug: schedule-post
      parameters:
      - in: formData
        name: campaignId
        description: The Campaign ID to use for this Event
      - in: formData
        name: commandId
        description: The Command ID to use for this Event
      - in: formData
        name: dayPartId
        description: The Day Part for this event
      - in: formData
        name: displayGroupIds
        description: The Display Group IDs for this event
      - in: formData
        name: displayOrder
        description: The display order for this event
      - in: formData
        name: eventTypeId
        description: The Event Type Id to use for this Event
      - in: formData
        name: fromDt
        description: The from date for this event
      - in: formData
        name: isPriority
        description: An integer indicating the priority of this event
      - in: formData
        name: recurrenceDetail
        description: The interval for the recurrence
      - in: formData
        name: recurrenceRange
        description: The end date for this events recurrence
      - in: formData
        name: recurrenceRepeatsOn
        description: The days of the week that this event repeats - weekly only
      - in: formData
        name: recurrenceType
        description: The type of recurrence to apply to this event
      - in: formData
        name: syncTimezone
        description: Should this schedule be synced to the resulting Display timezone?
      - in: formData
        name: toDt
        description: The to date for this event
      responses:
        200:
          description: OK
      tags:
      - Schedule
      - Event
  /schedule/{eventId}:
    put:
      summary: Edit Schedule Event
      description: Edit a scheduled event for a Campaign/Layout to be shown on a Display
        Group/Display.
      operationId: scheduleEdit
      x-api-path-slug: scheduleeventid-put
      parameters:
      - in: formData
        name: campaignId
        description: The Campaign ID to use for this Event
      - in: formData
        name: commandId
        description: The Command ID to use for this Event
      - in: formData
        name: dayPartId
        description: The Day Part for this event
      - in: formData
        name: displayGroupIds
        description: The Display Group IDs for this event
      - in: formData
        name: displayOrder
        description: The display order for this event
      - in: path
        name: eventId
        description: The Scheduled Event ID
      - in: formData
        name: eventTypeId
        description: The Event Type Id to use for this Event
      - in: formData
        name: fromDt
        description: The from date for this event
      - in: formData
        name: isPriority
        description: An integer indicating the priority of this event
      - in: formData
        name: recurrenceDetail
        description: The interval for the recurrence
      - in: formData
        name: recurrenceRange
        description: The end date for this events recurrence
      - in: formData
        name: recurrenceRepeatsOn
        description: The days of the week that this event repeats - weekly only
      - in: formData
        name: recurrenceType
        description: The type of recurrence to apply to this event
      - in: formData
        name: syncTimezone
        description: Should this schedule be synced to the resulting Display timezone?
      - in: formData
        name: toDt
        description: The to date for this event
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Schedule
      - Event
    delete:
      summary: Delete Event
      description: Delete a Scheduled Event
      operationId: scheduleDelete
      x-api-path-slug: scheduleeventid-delete
      parameters:
      - in: path
        name: eventId
        description: The Scheduled Event ID
      responses:
        200:
          description: OK
      tags:
      - Event
  /stats:
    get:
      summary: ""
      description: ""
      operationId: statsSearch
      x-api-path-slug: stats-get
      parameters:
      - in: formData
        name: displayId
        description: An optional display Id to filter
      - in: formData
        name: fromDt
        description: The start date for the filter
      - in: formData
        name: layoutId
        description: An optional array of layout Id to filter
      - in: formData
        name: mediaId
        description: An optional array of media Id to filter
      - in: formData
        name: toDt
        description: The end date for the filter
      - in: formData
        name: type
        description: The type of stat to return
      responses:
        200:
          description: OK
      tags:
      - ""
  /template:
    get:
      summary: Template Search
      description: Search templates this user has access to
      operationId: templateSearch
      x-api-path-slug: template-get
      responses:
        200:
          description: OK
      tags:
      - Template
      - Search
  /template/{layoutId}:
    post:
      summary: Add a template from a Layout
      description: Use the provided layout as a base for a new template
      operationId: template.add.from.layout
      x-api-path-slug: templatelayoutid-post
      parameters:
      - in: formData
        name: description
        description: A description of the Template
      - in: formData
        name: includeWidgets
        description: Flag indicating whether to include the widgets in the Template
      - in: path
        name: layoutId
        description: The Layout ID
      - in: formData
        name: name
        description: The Template Name
      - in: formData
        name: tags
        description: Comma separated list of Tags for the template
      responses:
        200:
          description: OK
      tags:
      - Template
      - From
      - Layout
  /user/me:
    get:
      summary: Get Me
      description: Get my details
      operationId: userMe
      x-api-path-slug: userme-get
      responses:
        200:
          description: OK
      tags:
      - Me
  /user:
    get:
      summary: User Search
      description: Search users
      operationId: userSearch
      x-api-path-slug: user-get
      parameters:
      - in: formData
        name: retired
        description: Filter by Retired
      - in: formData
        name: userId
        description: Filter by User Id
      - in: formData
        name: userName
        description: Filter by User Name
      - in: formData
        name: userTypeId
        description: Filter by UserType Id
      responses:
        200:
          description: OK
      tags:
      - User
      - Search
    post:
      summary: Add User
      description: Add a new User
      operationId: userAdd
      x-api-path-slug: user-post
      parameters:
      - in: formData
        name: email
        description: The user email address
      - in: formData
        name: firstName
        description: The users first name
      - in: formData
        name: groupId
        description: The inital user group for this User
      - in: formData
        name: homePageId
        description: The homepage to use for this User
      - in: formData
        name: lastName
        description: The users last name
      - in: formData
        name: libraryQuota
        description: The users library quota in kilobytes
      - in: formData
        name: password
        description: The users password
      - in: formData
        name: phone
        description: The users phone number
      - in: formData
        name: ref1
        description: Reference 1
      - in: formData
        name: ref2
        description: Reference 2
      - in: formData
        name: ref3
        description: Reference 3
      - in: formData
        name: ref4
        description: Reference 4
      - in: formData
        name: ref5
        description: Reference 5
      - in: formData
        name: userName
        description: The User Name
      - in: formData
        name: userTypeId
        description: The user type ID
      responses:
        200:
          description: OK
      tags:
      - User
  /user/permissions/{entity}/{objectId}:
    get:
      summary: Permission Data
      description: Permission data for the Entity and Object Provided.
      operationId: userPermissionsSearch
      x-api-path-slug: userpermissionsentityobjectid-get
      parameters:
      - in: path
        name: entity
        description: The Entity
      - in: path
        name: objectId
        description: The ID of the Object to return permissions for
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Data
    post:
      summary: Permission Set
      description: Set Permissions to users/groups for the provided entity.
      operationId: userPermissionsSet
      x-api-path-slug: userpermissionsentityobjectid-post
      parameters:
      - in: path
        name: entity
        description: The Entity
      - in: formData
        name: groupIds
        description: Array of permissions with groupId as the key
      - in: path
        name: objectId
        description: The ID of the Object to set permissions on
      - in: formData
        name: ownerId
        description: Change the owner of this item
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Set
  /user/pref:
    get:
      summary: Retrieve User Preferences
      description: User preferences for non-state information, such as Layout designer
        zoom levels
      operationId: userPrefGet
      x-api-path-slug: userpref-get
      parameters:
      - in: formData
        name: preference
        description: An optional preference
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - User
      - Preferences
    post:
      summary: Save User Preferences
      description: Save User preferences for non-state information, such as Layout
        designer zoom levels
      operationId: userPrefEdit
      x-api-path-slug: userpref-post
      parameters:
      - in: body
        name: preference
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Save
      - User
      - Preferences
  /usergroup:
    get:
      summary: UserGroup Search
      description: Search User Groups
      operationId: userGroupSearch
      x-api-path-slug: usergroup-get
      parameters:
      - in: formData
        name: userGroup
        description: Filter by UserGroup Name
      - in: formData
        name: userGroupId
        description: Filter by UserGroup Id
      responses:
        200:
          description: OK
      tags:
      - UserGroup
      - Search
  /group/{userGroupId}/copy:
    post:
      summary: Copy User Group
      description: Copy an user group, optionally copying the group members
      operationId: userGroupCopy
      x-api-path-slug: groupusergroupidcopy-post
      parameters:
      - in: formData
        name: copyMembers
        description: Flag indicating whether to copy group members
      - in: formData
        name: group
        description: The Group Name
      - in: path
        name: userGroupId
        description: The User Group ID to Copy
      responses:
        200:
          description: OK
      tags:
      - Copy
      - User
      - Group
  /playlist/widget/audio/{playlistId}:
    post:
      summary: Parameters for editing existing audio widget on a layout
      description: Parameters for editing existing audio widget on a layout, for adding
        new audio, please refer to POST /library documentation
      operationId: WidgetAudioEdit
      x-api-path-slug: playlistwidgetaudioplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: loop
        description: Edit only - Flag (0, 1) Should the audio loop (only for duration
          > 0 )?
      - in: formData
        name: mute
        description: Edit only - Flag (0, 1) Should the audio be muted?
      - in: formData
        name: name
        description: Edit Only - The Widget name
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Audio
      - Widget
      - "On"
      - Layout
  /playlist/widget/chart/{playlistId}:
    post:
      summary: Add a Chart Widget
      description: Add a new Chart Widget to the specified playlist
      operationId: WidgetChartAdd
      x-api-path-slug: playlistwidgetchartplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: EDIT Only - Background Color
      - in: formData
        name: columnType
        description: EDIT only - Array of Column Types (x-axis, y-axis, series-identifier)
          to assign
      - in: formData
        name: dataSetColumnId
        description: EDIT only - Array of dataSetColumn IDs to assign
      - in: formData
        name: dataSetId
        description: Create Chart Widget using provided dataSetId of an existing dataSet
      - in: formData
        name: duration
        description: EDIT Only - The Chart Duration
      - in: formData
        name: filter
        description: EDIT Only - SQL clause for filter this dataSet
      - in: formData
        name: fontColor
        description: EDIT Only - Font Color
      - in: formData
        name: fontSize
        description: EDIT Only - Font Size
      - in: formData
        name: graphType
        description: EDIT only - Chart Type
      - in: formData
        name: legendPosition
        description: EDIT Only - Where should the Legend be Shown (top, left, right,
          bottom)
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: ordering
        description: EDIT Only - SQL clause for how this dataSet should be ordered
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: showLegend
        description: EDIT Only - Should the Legend be Shown
      - in: formData
        name: startYAtZero
        description: EDIT Only - Start the Y-Axis at 0
      - in: formData
        name: title
        description: EDIT Only - Chart title
      - in: formData
        name: updateInterval
        description: EDIT Only - Update interval in minutes
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      - in: formData
        name: useFilteringClause
        description: EDIT Only - flag (0,1) Use advanced filter clause - set to 1
          if filter is provided
      - in: formData
        name: useOrderingClause
        description: EDIT Only - flag (0,1) Use advanced order clause - set to 1 if
          ordering is provided
      - in: formData
        name: x-axis-label
        description: EDIT Only - Chart x-axis label
      - in: formData
        name: y-axis-label
        description: EDIT Only - Chart y-axis label
      responses:
        200:
          description: OK
      tags:
      - Chart
      - Widget
  /playlist/widget/clock/{playlistId}:
    post:
      summary: Add a Clock Widget
      description: Add a new Clock Widget to the specified playlist
      operationId: WidgetClockAdd
      x-api-path-slug: playlistwidgetclockplaylistid-post
      parameters:
      - in: formData
        name: ClockFace
        description: 'For Flip Clock, supported options: TwelveHourClock TwentyFourHourClock
          HourlyCounter MinuteCounter DailyCounter'
      - in: formData
        name: clockTypeId
        description: Type of a clock widget 1-Analogue, 2-Digital, 3-Flip clock
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: format
        description: For digital clock, format in which the time should be displayed
          example [HH:mm]
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: offset
        description: The offset in minutes that should be applied to the current time,
          if a counter is selected then date/time to run from in the format Y-m-d
          H:i:s
      - in: path
        name: playlistId
        description: The playlist ID to add a Clock widget to
      - in: formData
        name: showSeconds
        description: For Flip Clock, should the clock show seconds or not
      - in: formData
        name: themeId
        description: Flag (0 , 1) for Analogue clock the light and dark theme
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Clock
      - Widget
  /playlist/widget/currencies/{playlistId}:
    post:
      summary: Add a Currencies Widget
      description: Add a new Currencies Widget to the specified playlist
      operationId: WidgetCurrenciesAdd
      x-api-path-slug: playlistwidgetcurrenciesplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: base
        description: The base currency
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerPage
        description: A flag (0, 1), The duration specified is per page/item, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: items
        description: Items wanted
      - in: formData
        name: itemtemplate
        description: Template for each item, replaces [itemsTemplate] in main template,
          Pass only with overrideTemplate set to 1
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: mainTemplate
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: maxItemsPerPage
        description: This is the intended number of items on each page
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noRecordsMessage
        description: A message to display when there are no records returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Currencies widget
      - in: formData
        name: reverseConversion
        description: (0, 1) Select 1 if youd like your base currency to be used as
          the comparison currency youve entered
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: currencies1,
          currencies2'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: widgetOriginalHeight
        description: This is the intended Height of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalWidth
        description: This is the intended Width of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      responses:
        200:
          description: OK
      tags:
      - Currencies
      - Widget
  /playlist/widget/dataSetView/{playlistId}:
    post:
      summary: Add a dataSetView Widget
      description: Add a new dataSetView Widget to the specified playlist
      operationId: WidgetdataSetViewAdd
      x-api-path-slug: playlistwidgetdatasetviewplaylistid-post
      parameters:
      - in: formData
        name: dataSetColumnId
        description: EDIT only - Array of dataSetColumn IDs to assign
      - in: formData
        name: dataSetId
        description: Create dataSetView Widget using provided dataSetId of an existing
          dataSet
      - in: formData
        name: duration
        description: EDIT Only - The dataSetView Duration
      - in: formData
        name: filter
        description: EDIT Only - SQL clause for filter this dataSet
      - in: formData
        name: lowerLimit
        description: EDIT Only - Lower low limit for this dataSet, 0 for nor limit
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noDataMessage
        description: EDIT Only - A message to display when no data is returned from
          the source
      - in: formData
        name: ordering
        description: EDIT Only - SQL clause for how this dataSet should be ordered
      - in: formData
        name: overrideTemplate
        description: EDIT Only - flag (0, 1) override template checkbox
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: rowsPerPage
        description: EDIT Only - Number of rows per page, 0 for no pages
      - in: formData
        name: showHeadings
        description: EDIT Only - Should the table show Heading? (0,1)
      - in: formData
        name: templateId
        description: 'EDIT Only - Template youd like to apply, options available:
          empty, light-green'
      - in: formData
        name: updateInterval
        description: EDIT Only - Update interval in minutes
      - in: formData
        name: upperLimit
        description: EDIT Only - Upper low limit for this dataSet, 0 for nor limit
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      - in: formData
        name: useFilteringClause
        description: EDIT Only - flag (0,1) Use advanced filter clause - set to 1
          if filter is provided
      - in: formData
        name: useOrderingClause
        description: EDIT Only - flag (0,1) Use advanced order clause - set to 1 if
          ordering is provided
      responses:
        200:
          description: OK
      tags:
      - DataSetView
      - Widget
  /playlist/widget/embedded/{playlistId}:
    post:
      summary: Add a Embedded Widget
      description: Add a new Embedded Widget to the specified playlist
      operationId: WidgetEmbeddedAdd
      x-api-path-slug: playlistwidgetembeddedplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: embedHtml
        description: HTML to embed
      - in: formData
        name: embedScript
        description: HEAD content to Embed (including script tags)
      - in: formData
        name: embedStyle
        description: Custom Style Sheets (CSS)
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add an Embedded Widget
      - in: formData
        name: scaleContent
        description: Flag (0,1) - Should the embedded content be scaled along with
          the layout?
      - in: formData
        name: transparency
        description: Flag (0,1) - Should the HTML be shown with transparent background?
          - not available on Windows Clients
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Embedded
      - Widget
  /playlist/widget/finance/{playlistId}:
    post:
      summary: Add a Finance Widget
      description: Add a new Finance Widget to the specified playlist
      operationId: WidgetFinanceAdd
      x-api-path-slug: playlistwidgetfinanceplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per item, otherwise
          the widget duration is divided between the number of items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft'
      - in: formData
        name: item
        description: Items wanted, can be comma separated (example EURUSD, GBPUSD),
          pass only with overrideTemplate set to 1
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noRecordsMessage
        description: A message to display when there are no records returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Finance widget
      - in: formData
        name: resultIdentifier
        description: The name of the result identifier returned by the YQL, pass only
          with overrideTemplate set to 1
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal) or the Marquee speed in a low to high scale (normal = 1)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: template
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: currency-simple,
          stock-simple'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: yql
        description: The YQL query to use for data, pass only with overrideTemplate
          set to 1
      responses:
        200:
          description: OK
      tags:
      - Finance
      - Widget
  /playlist/widget/forecastIo/{playlistId}:
    post:
      summary: Add a Weather Widget
      description: Add a new Weather Widget to the specified playlist
      operationId: WidgetWeatherAdd
      x-api-path-slug: playlistwidgetforecastioplaylistid-post
      parameters:
      - in: formData
        name: currentTemplate
        description: Current template, Pass only with overrideTemplate set to 1
      - in: formData
        name: dailyTemplate
        description: Replaces [dailyForecast] in main template, Pass only with overrideTemplate
          set to 1
      - in: formData
        name: dayConditionsOnly
        description: Flag (0, 1) Would you like to only show the Daytime weather conditions
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: lang
        description: Language youd like to use, supported languages ar, az, be, bs,
          cs, de, en, el, es, fr, hr, hu, id, it, is, kw, nb, nl, pl, pt, ru, sk,
          sr, sv, tet, tr, uk, x-pig-latin, zh, zh-tw
      - in: formData
        name: latitude
        description: The latitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: longitude
        description: The longitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Weather widget
      - in: formData
        name: styleSheet
        description: Optional StyleSheet, Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: weather-module0-5day,
          weather-module0-singleday, weather-module0-singleday2, weather-module1l,
          weather-module1p, weather-module2l, weather-module2p, weather-module3l,
          weather-module3p, weather-module4l, weather-module4p, weather-module5l,
          weather-module6v, weather-module6h'
      - in: formData
        name: units
        description: 'Units you would like to use, available options: auto, ca, si,
          uk2, us'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDisplayLocation
        description: Flag (0, 1) Use the location configured on display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: widgetOriginalHeight
        description: This is the intended Height of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalWidth
        description: This is the intended Width of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Widget
  /playlist/widget/googleTraffic/{playlistId}:
    post:
      summary: Add a Google Traffic Widget
      description: Add a new Google traffic Widget to the specified playlist
      operationId: WidgetGoogleTrafficAdd
      x-api-path-slug: playlistwidgetgoogletrafficplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: latitude
        description: The latitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: longitude
        description: The longitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget
      - in: formData
        name: useDisplayLocation
        description: Flag (0, 1) Use the location configured on display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: zoom
        description: How far should the map be zoomed in? The higher the number the
          closer the zoom, 1 represents entire globe
      responses:
        200:
          description: OK
      tags:
      - Google
      - Traffic
      - Widget
  /playlist/widget/hls/{playlistId}:
    post:
      summary: Add a HLS Widget
      description: Add a new HLS Widget to the specified playlist
      operationId: WidgetHlsAdd
      x-api-path-slug: playlistwidgethlsplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: mute
        description: Flag (0, 1) Should the video be muted?
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: transparency
        description: Flag (0, 1), This causes some android devices to switch to a
          hardware accelerated web view
      - in: formData
        name: uri
        description: URL to HLS video stream
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select only if you will provide duration parameter
          as well
      responses:
        200:
          description: OK
      tags:
      - HLS
      - Widget
  /playlist/widget/image/{playlistId}:
    post:
      summary: Parameters for editing existing image on a layout
      description: Parameters for editing existing image on a layout, for adding new
        images, please refer to POST /library documentation
      operationId: WidgetImageEdit
      x-api-path-slug: playlistwidgetimageplaylistid-post
      parameters:
      - in: formData
        name: alignId
        description: Edit only - Horizontal alignment - left, center, bottom
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: name
        description: Edit only - Optional Widget Name
      - in: formData
        name: scaleTypeId
        description: 'Edit only - Select scale type available options: center, stretch'
      - in: formData
        name: useDuration
        description: Edit only (0, 1) Select 1 only if you will provide duration parameter
          as well
      - in: formData
        name: valignId
        description: Edit only - Vertical alignment - top, middle, bottom
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Image
      - "On"
      - Layout
  /playlist/widget/localVideo/{playlistId}:
    post:
      summary: Add a Local Video Widget
      description: Add a new Local Video Widget to the specified playlist
      operationId: WidgetLocalVideoAdd
      x-api-path-slug: playlistwidgetlocalvideoplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: mute
        description: Flag (0, 1) Should the video be muted?
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: scaleTypeId
        description: 'How should the video be scaled, available options: aspect, stretch'
      - in: formData
        name: uri
        description: A local file path or URL to the video
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Local
      - Video
      - Widget
  /playlist/widget/notificationview/{playlistId}:
    post:
      summary: Add a Notification Widget
      description: Add a new Notification Widget to the specified playlist
      operationId: WidgetNotificationAdd
      x-api-path-slug: playlistwidgetnotificationviewplaylistid-post
      parameters:
      - in: formData
        name: age
        description: The maximum notification age in minutes - 0 for all
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per page/item, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: embedStyle
        description: Custom Style Sheets (CSS)
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noDataMessage
        description: Message to show when no notifications are available
      - in: path
        name: playlistId
        description: The playlist ID to add an Notification Widget
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Widget
  /playlist/widget/pdf/{playlistId}:
    post:
      summary: Parameters for editing existing pdf on a layout
      description: Parameters for editing existing pdf on a layout, for adding new
        files, please refer to POST /library documentation
      operationId: WidgetPdfEdit
      x-api-path-slug: playlistwidgetpdfplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: name
        description: Edit only - Optional Widget Name
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Pdf
      - "On"
      - Layout
  /playlist/widget/shellCommand/{playlistId}:
    post:
      summary: Add a Shell Command Widget
      description: Add a new Shell Command Widget to the specified playlist
      operationId: WidgetShellCommandAdd
      x-api-path-slug: playlistwidgetshellcommandplaylistid-post
      parameters:
      - in: formData
        name: commandCode
        description: Enter a reference code for exiting command in CMS
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: launchThroughCmd
        description: flag (0,1) Windows only, Should the player launch this command
          through the windows command line (cmd
      - in: formData
        name: linuxCommand
        description: Enter a Android / Linux command line compatible command
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: terminateCommand
        description: flag (0,1) Should the player forcefully terminate the command
          after the duration specified, 0 to let the command terminate naturally
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: useTaskkill
        description: flag (0,1) Windows only, should the player use taskkill to terminate
          commands
      - in: formData
        name: windowsCommand
        description: Enter a Windows command line compatible command
      responses:
        200:
          description: OK
      tags:
      - Shell
      - Command
      - Widget
  /playlist/widget/stocks/{playlistId}:
    post:
      summary: Add a Stocks Widget
      description: Add a new Stocks Widget to the specified playlist
      operationId: WidgetStocksAdd
      x-api-path-slug: playlistwidgetstocksplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerPage
        description: A flag (0, 1), The duration specified is per page, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: items
        description: Items wanted, can be comma separated
      - in: formData
        name: itemtemplate
        description: Template for each item, replaces [itemsTemplate] in main template,
          Pass only with overrideTemplate set to 1
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: mainTemplate
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: maxItemsPerPage
        description: This is the intended number of items on each page
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noRecordsMessage
        description: A message to display when there are no records returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Stocks widget
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: stocks1, stocks2'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Stocks
      - Widget
  /playlist/widget/text/{playlistId}:
    post:
      summary: Add a Text Widget
      description: Add a new Text Widget to the specified playlist
      operationId: WidgetTextAdd
      x-api-path-slug: playlistwidgettextplaylistid-post
      parameters:
      - in: formData
        name: backgroundcolor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft'
      - in: formData
        name: javaScript
        description: Optional JavaScript
      - in: formData
        name: marqueeInlineSelector
        description: The selector to use for stacking marquee items in a line when
          scrolling left/right
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal) or the Marquee speed in a low to high scale (normal = 1)
      - in: formData
        name: text
        description: Enter the text to display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Text
      - Widget
  /playlist/widget/ticker/{playlistId}:
    post:
      summary: Add a ticker Widget
      description: Add a new ticker Widget to the specified playlist
      operationId: WidgetTickerAdd
      x-api-path-slug: playlistwidgettickerplaylistid-post
      parameters:
      - in: formData
        name: allowedAttributes
        description: EDIT Only and SourceId=1 - A comma separated list of attributes
          that should not be stripped from the feed
      - in: formData
        name: backgroundColor
        description: Edit only - A HEX color to use as the background color of this
          widget
      - in: formData
        name: copyright
        description: EDIT Only and SourceId=1 - Copyright information to display as
          the last item in this feed
      - in: formData
        name: css
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
          or with sourceId=2
      - in: formData
        name: dataSetId
        description: For sourceId=2, Create ticker Widget using provided dataSetId
          of an existing dataSet
      - in: formData
        name: dateFormat
        description: EDIT Only - The date format to apply to all dates returned by
          the ticker
      - in: formData
        name: disableDateSort
        description: EDIT Only, SourceId=1 - Should the date sort applied to the feed
          be disabled?
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per item, otherwise
          it is per feed
      - in: formData
        name: effect
        description: 'Edit only - Effect that will be used to transitions between
          items, available options: fade, fadeout, scrollVert, scollHorz, flipVert,
          flipHorz, shuffle, tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight,
          marqueeLeft'
      - in: formData
        name: filter
        description: EDIT Only, SourceId=2 - SQL clause for filter this dataSet
      - in: formData
        name: itemsPerPage
        description: EDIT Only - When in single mode, how many items per page should
          be shown
      - in: formData
        name: itemsSideBySide
        description: A flag (0, 1), Should items be shown side by side
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: lowerLimit
        description: EDIT Only, SourceId=2 - Lower low limit for this dataSet, 0 for
          nor limit
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noDataMessage
        description: EDIT Only - A message to display when no data is returned from
          the source
      - in: formData
        name: numItems
        description: EDIT Only and SourceId=1 - The number of RSS items you want to
          display
      - in: formData
        name: ordering
        description: EDIT Only, SourceId=2- SQL clause for how this dataSet should
          be ordered
      - in: formData
        name: overrideTemplate
        description: EDIT Only, SourceId=1 - flag (0, 1) override template checkbox
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: randomiseItems
        description: A flag (0, 1), whether to randomise the feed
      - in: formData
        name: sourceId
        description: Add only - 1 for rss feed, 2 for dataset
      - in: formData
        name: speed
        description: Edit only - The transition speed of the selected effect in milliseconds
          (1000 = normal) or the Marquee speed in a low to high scale (normal = 1)
      - in: formData
        name: stripTags
        description: EDIT Only and SourceId=1 - A comma separated list of attributes
          that should be stripped from the feed
      - in: formData
        name: takeItemsFrom
        description: 'EDIT Only and SourceId=1 - Take the items form the beginning
          or the end of the list, available options: start, end'
      - in: formData
        name: template
        description: Template for each item, replaces [itemsTemplate] in main template,
          Pass only with overrideTemplate set to 1 or with sourceId=2
      - in: formData
        name: templateId
        description: 'EDIT Only, SourceId=1 - Template youd like to apply, options
          available: title-only, prominent-title-with-desc-and-name-separator, media-rss-with-title,
          media-rss-wth-left-hand-text, media-rss-image-only'
      - in: formData
        name: textDirection
        description: 'EDIT Only, SourceId=1 - Which direction does the text in the
          feed use? Available options: ltr, rtl'
      - in: formData
        name: updateInterval
        description: EDIT Only - Update interval in minutes
      - in: formData
        name: upperLimit
        description: EDIT Only, SourceId=2 - Upper low limit for this dataSet, 0 for
          nor limit
      - in: formData
        name: uri
        description: For sourceId=1, the link for the rss feed
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: useFilteringClause
        description: EDIT Only, SourceId=2 - flag (0,1) Use advanced filter clause
          - set to 1 if filter is provided
      - in: formData
        name: useOrderingClause
        description: EDIT Only, SourceId=2 - flag (0,1) Use advanced order clause
          - set to 1 if ordering is provided
      responses:
        200:
          description: OK
      tags:
      - Ticker
      - Widget
  /playlist/widget/twitter/{playlistId}:
    post:
      summary: Add a Twitter Widget
      description: Add a new Twitter Widget to the specified playlist
      operationId: WidgetTwitterAdd
      x-api-path-slug: playlistwidgettwitterplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per page/item, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: itemsPerPage
        description: EDIT Only - When in single mode, how many items per page should
          be shown
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: language
        description: Language in which tweets should be returned
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noTweetsMessage
        description: A message to display when there are no tweets returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Twitter widget
      - in: formData
        name: removeHashtags
        description: Flag (0, 1) Should the hashtags (#something) be removed from
          the tweet text
      - in: formData
        name: removeMentions
        description: Flag (0, 1) Should mentions (@someone) be removed from the tweet
          text?
      - in: formData
        name: removeUrls
        description: Flag (0, 1) Should the URLs be removed from the tweet text?
      - in: formData
        name: resultContent
        description: 'Intended content Type, available Options: 0 - All Tweets 1 -
          Tweets with the text only content 2 - Tweets with the text and image content'
      - in: formData
        name: resultType
        description: 1 - Mixed, 2 -Recent 3 - Popular, Recent shows only recent tweets,
          Popular the most popular tweets and Mixed included both popular and recent
      - in: formData
        name: searchTerm
        description: Twitter search term, you can test your search term in twitter
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: template
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: full-timeline-np,
          full-timeline, tweet-only, tweet-with-profileimage-left, tweet-with-profileimage-right,
          tweet-1, tweet-2, tweet-4'
      - in: formData
        name: tweetCount
        description: The number of tweets to return
      - in: formData
        name: tweetDistance
        description: Distance in miles that the tweets should be returned from
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: widgetOriginalHeight
        description: This is the intended Height of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalPadding
        description: This is the intended Padding of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalWidth
        description: This is the intended Width of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      responses:
        200:
          description: OK
      tags:
      - Twitter
      - Widget
  /playlist/widget/twittermetro/{playlistId}:
    post:
      summary: Add a Twitter Metro Widget
      description: Add a new Twitter Metro Widget to the specified playlist
      operationId: WidgetTwitterMetroAdd
      x-api-path-slug: playlistwidgettwittermetroplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: colorTemplateId
        description: 'Use pre-configured templates, available options: default, full,
          gray, light, soft, vivid'
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: language
        description: Language in which tweets should be returned
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noTweetsMessage
        description: A message to display when there are no tweets returned by the
          search query
      - in: formData
        name: overrideColorTemplate
        description: flag (0, 1) set to 0 and use colorTemplateId or set to 1 and
          provide colours to use in templateColours parameter
      - in: path
        name: playlistId
        description: The playlist ID to add a Twitter Metro widget
      - in: formData
        name: removeHashtags
        description: Flag (0, 1) Should the hashtags (#something) be removed from
          the tweet text
      - in: formData
        name: removeMentions
        description: Flag (0, 1) Should mentions (@someone) be removed from the tweet
          text?
      - in: formData
        name: removeRetweets
        description: Flag (0, 1) Should retweets be filtered?
      - in: formData
        name: removeUrls
        description: Flag (0, 1) Should the URLs be removed from the tweet text?
      - in: formData
        name: resultContent
        description: 'Intended content Type, available Options: 0 - All Tweets 1 -
          Tweets with the text only content 2 - Tweets with the text and image content'
      - in: formData
        name: resultType
        description: 1 - Mixed, 2 -Recent 3 - Popular, Recent shows only recent tweets,
          Popular the most popular tweets and Mixed included both popular and recent
      - in: formData
        name: searchTerm
        description: Twitter search term, you can test your search term in twitter
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: templateColours
        description: 'Provide a string of new HEX colour codes to use, separated by
          |, for example: #e0d2c8|#5e411d|#fccf12|#82ff00|#64bae8'
      - in: formData
        name: tweetCount
        description: The number of tweets to return
      - in: formData
        name: tweetDistance
        description: Distance in miles that the tweets should be returned from
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Twitter
      - Metro
      - Widget
  /playlist/widget/video/{playlistId}:
    post:
      summary: Parameters for editing existing video on a layout
      description: Parameters for editing existing video on a layout, for adding new
        videos, please refer to POST /library documentation
      operationId: WidgetVideoEdit
      x-api-path-slug: playlistwidgetvideoplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: loop
        description: Edit only - Flag (0, 1) Should the video loop (only for duration
          > 0 )?
      - in: formData
        name: mute
        description: Edit only - Flag (0, 1) Should the video be muted?
      - in: formData
        name: name
        description: Edit only - Optional Widget Name
      - in: formData
        name: scaleTypeId
        description: 'How should the video be scaled, available options: aspect, stretch'
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Video
      - "On"
      - Layout
  /playlist/widget/videoin/{playlistId}:
    post:
      summary: Add a Video In Widget
      description: Add a new Video In Widget to the specified playlist
      operationId: WidgetVideoInAdd
      x-api-path-slug: playlistwidgetvideoinplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: sourceId
        description: 'Which device input should be shown? available options: HDMI,
          RGB, DVI, DP, OPS'
      - in: formData
        name: useDuration
        description: Flag (0, 1) Select only if you will provide duration parameter
          as well
      responses:
        200:
          description: OK
      tags:
      - Video
      - In
      - Widget
  /playlist/widget/webpage/{playlistId}:
    post:
      summary: Add a Web page Widget
      description: Add a new Web page Widget to the specified playlist
      operationId: WidgetWebpageAdd
      x-api-path-slug: playlistwidgetwebpageplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Web page Duration
      - in: formData
        name: modeId
        description: The mode option for Web page, 1- Open Natively, 2- Manual Position,
          3- Best Ft
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: offsetLeft
        description: For Manual position, the starting point from the left in pixels
      - in: formData
        name: offsetTop
        description: For Manual position, the starting point from the Top in pixels
      - in: formData
        name: pageHeight
        description: For Manual Position and Best Fit, The height of the page - if
          empty it will use region height
      - in: formData
        name: pageWidth
        description: For Manual Position and Best Fit, The width of the page - if
          empty it will use region width
      - in: path
        name: playlistId
        description: The playlist ID to add a Web page to
      - in: formData
        name: scaling
        description: For Manual position the percentage to scale the Web page (0-100)
      - in: formData
        name: transparency
        description: flag (0,1) should the HTML be shown with a transparent background?
      - in: formData
        name: uri
        description: string containing the location (URL) of the web page
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Web
      - Page
      - Widget
---