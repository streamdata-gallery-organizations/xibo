---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Daypart Add
  description: Add a Daypart
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