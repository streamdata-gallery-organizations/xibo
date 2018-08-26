{
  "info": {
    "name": "Xibo API Action: Overlay Layout",
    "_postman_id": "511cd1ef-4883-4a4f-9a54-25e8f347b911",
    "description": "Send the overlay layout action to this DisplayGroup",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Action:",
      "item": [
        {
          "id": "62c11b9a-5b68-403d-a0b7-5533b0346d50",
          "name": "displayGroupActionCollectNow",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/collectNow"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
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
            "description": "Send the collect now action to this DisplayGroup"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "647d99f9-80b3-42e7-bf88-14985a97d957"
            }
          ]
        },
        {
          "id": "29c9adbe-bd8d-47e2-a4a5-e18039dba6a4",
          "name": "displayGroupActionClearStatsAndLogs",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/clearStatsAndLogs"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
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
            "description": "Clear all stats and logs on this Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6665c7b5-aaf7-4432-8292-7e98cecd2da1"
            }
          ]
        },
        {
          "id": "44cf32d7-d753-46f4-b4c1-97713d8ff028",
          "name": "displayGroupActionChangeLayout",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/changeLayout"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
                  "key": "changeMode",
                  "value": "{}",
                  "disabled": false,
                  "description": "Whether to queue or replace with this action"
                },
                {
                  "key": "downloadRequired",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether the player should perform a collect before playing the Layout"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The duration in seconds for this Layout change to remain in effect"
                },
                {
                  "key": "layoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Layout Id"
                }
              ]
            },
            "description": "Send the change layout action to this DisplayGroup"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a5a2818c-6c64-4736-b1ea-7a69c17e3ab1"
            }
          ]
        },
        {
          "id": "cab0f39f-48e5-4cdf-8964-d2735d45ffda",
          "name": "displayGroupActionRevertToSchedule",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/revertToSchedule"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
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
            "description": "Send the revert to schedule action to this DisplayGroup"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f4f1847-a27e-4144-8517-0fd028a2f1ec"
            }
          ]
        },
        {
          "id": "5bbff9d5-e822-4b09-8747-e25dabf359e0",
          "name": "displayGroupActionOverlayLayout",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/overlayLayout"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
                  "key": "downloadRequired",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether the player should perform a collect before adding the Overlay"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The duration in seconds for this Overlay to remain in effect"
                },
                {
                  "key": "layoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Layout Id"
                }
              ]
            },
            "description": "Send the overlay layout action to this DisplayGroup"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e1903171-01a0-43f0-9ca1-d5de7a63da80"
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