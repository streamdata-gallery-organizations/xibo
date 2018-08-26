{
  "info": {
    "name": "Xibo API Delete a Display Group",
    "_postman_id": "a9dd961c-2988-4192-9e2c-76e635f5f6bf",
    "description": "Delete an existing Display Group identified by its Id",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Display",
      "item": [
        {
          "id": "83542656-41be-4cc0-9596-d89d32580304",
          "name": "displaySearch",
          "request": {
            "url": "{{default}}/display",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Search Displays for this User"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "79ec60f2-34f3-4f3d-852a-da13c4645590"
            }
          ]
        },
        {
          "id": "dabba10c-56d1-42b4-ba11-278b57367e09",
          "name": "displayEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "display/:displayId"
              ],
              "variable": [
                {
                  "id": "displayId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "alertTimeout",
                  "value": "{}",
                  "disabled": false,
                  "description": "How long in seconds should this display wait before alerting when it hasnt connected"
                },
                {
                  "key": "auditingUntil",
                  "value": "{}",
                  "disabled": false,
                  "description": "A date this Display records auditing information until"
                },
                {
                  "key": "broadCastAddress",
                  "value": "{}",
                  "disabled": false,
                  "description": "The BroadCast Address for this Display - used by Wake On LAN"
                },
                {
                  "key": "cidr",
                  "value": "{}",
                  "disabled": false,
                  "description": "The CIDR configuration for this Display"
                },
                {
                  "key": "clearCachedData",
                  "value": "{}",
                  "disabled": false,
                  "description": "Clear all Cached data for this display"
                },
                {
                  "key": "defaultLayoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "A Layout ID representing the Default Layout for this Display"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "A description of the Display"
                },
                {
                  "key": "display",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Display Name"
                },
                {
                  "key": "displayProfileId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Display Settings Profile ID"
                },
                {
                  "key": "emailAlert",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether the Display generates up/down email alerts"
                },
                {
                  "key": "incSchedule",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether the Default Layout should be included in the Schedule"
                },
                {
                  "key": "latitude",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Latitude of this Display"
                },
                {
                  "key": "license",
                  "value": "{}",
                  "disabled": false,
                  "description": "The hardwareKey to use as the licence key for this Display"
                },
                {
                  "key": "licensed",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this display is licensed"
                },
                {
                  "key": "longitude",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Longitude of this Display"
                },
                {
                  "key": "rekeyXmr",
                  "value": "{}",
                  "disabled": false,
                  "description": "Clear the cached XMR configuration and send a rekey"
                },
                {
                  "key": "secureOn",
                  "value": "{}",
                  "disabled": false,
                  "description": "The secure on configuration for this Display"
                },
                {
                  "key": "tags",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of tags for this item"
                },
                {
                  "key": "timeZone",
                  "value": "{}",
                  "disabled": false,
                  "description": "The timezone for this display, or empty to use the CMS timezone"
                },
                {
                  "key": "wakeOnLanEnabled",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating if Wake On LAN is enabled for this Display"
                },
                {
                  "key": "wakeOnLanTime",
                  "value": "{}",
                  "disabled": false,
                  "description": "A h:i string representing the time that the Display should receive its Wake on LAN command"
                }
              ]
            },
            "description": "Edit a Display"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e9a259ed-5b69-4b7e-acf4-13ae1ead310f"
            }
          ]
        },
        {
          "id": "0e9b8738-70bd-4abd-be9b-189b12b05554",
          "name": "displayDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "display/:displayId"
              ],
              "variable": [
                {
                  "id": "displayId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Delete a Display"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4c0fe7a1-4fcb-4071-b9a9-fa83b67aa044"
            }
          ]
        },
        {
          "id": "52ef46b9-0fb1-4885-87e5-16a5b24ce36b",
          "name": "displayGroupSearch",
          "request": {
            "url": "{{default}}/displaygroup",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get Display Groups"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1c6b387c-5a29-421e-a14e-2bc7bc6e4f45"
            }
          ]
        },
        {
          "id": "19bbd108-87ec-426e-8867-bacfff2b1476",
          "name": "displayGroupAdd",
          "request": {
            "url": "{{default}}/displaygroup",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Display Group Description"
                },
                {
                  "key": "displayGroup",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Display Group Name"
                },
                {
                  "key": "dynamicContent",
                  "value": "{}",
                  "disabled": false,
                  "description": "The filter criteria for this dynamic group"
                },
                {
                  "key": "isDynamic",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this DisplayGroup is Dynamic"
                },
                {
                  "key": "tags",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of tags for this item"
                }
              ]
            },
            "description": "Add a new Display Group to the CMS"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3727dd1e-ffbb-440e-bbe3-16ce7e092e8c"
            }
          ]
        },
        {
          "id": "6fad9e34-9576-42ef-b099-d0a28adfa6e7",
          "name": "displayGroupDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Delete an existing Display Group identified by its Id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9105e96d-d973-4110-87ef-44bda7dbb20f"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "570f14f9-50f0-4e03-9c3f-c125e41b92b2",
          "name": "displayGroupEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Display Group Description"
                },
                {
                  "key": "displayGroup",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Display Group Name"
                },
                {
                  "key": "dynamicCriteria",
                  "value": "{}",
                  "disabled": false,
                  "description": "The filter criteria for this dynamic group"
                },
                {
                  "key": "isDynamic",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this DisplayGroup is Dynamic"
                },
                {
                  "key": "tags",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of tags for this item"
                }
              ]
            },
            "description": "Edit an existing Display Group identified by its Id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e05e1ec-7531-4ca8-83df-1e4853843ff8"
            }
          ]
        }
      ]
    }
  ],
  "variable": [
    {
      "key": "default",
      "value": "http://www.example.com/api"
    }
  ]
}