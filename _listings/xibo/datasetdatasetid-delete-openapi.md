---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Delete DataSet
  description: Delete a DataSet
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