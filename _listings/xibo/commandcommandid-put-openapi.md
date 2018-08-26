---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Edit Command
  description: Edit the provided command
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