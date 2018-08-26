---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Search Campaigns
  description: Search all Campaigns this user has access to
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