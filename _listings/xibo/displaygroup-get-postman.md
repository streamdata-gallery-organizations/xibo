{
  "info": {
    "name": "Xibo API Get Display Groups",
    "_postman_id": "e7c6b7f1-ad1b-4628-bdc8-99026db26ec1",
    "description": "",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Display",
      "item": [
        {
          "id": "c11756ee-091c-4aa7-98d7-788108e392c8",
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
              "id": "066f178f-c55c-4c53-aa24-c8ae71745a7d"
            }
          ]
        },
        {
          "id": "e28f0b67-0a60-46ff-a9af-ec84a15ef5a4",
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
              "id": "89e74eec-c2ce-498a-b08d-daaa1d2a213a"
            }
          ]
        },
        {
          "id": "032abb70-76a7-47d2-bc19-54e26b4e25ea",
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
              "id": "37e6ccfa-c5b7-418b-81d9-e1627c415cd3"
            }
          ]
        },
        {
          "id": "a04ca929-5d2e-449d-a3e2-52b51a8884fa",
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
              "id": "4faef669-4cde-4bcc-8d93-f604a2529ee0"
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