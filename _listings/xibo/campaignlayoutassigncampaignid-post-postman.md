{
  "info": {
    "name": "Xibo API Assign Layouts",
    "_postman_id": "31f5151b-c38d-4d2f-8c6f-e196a70f3423",
    "description": "Assign Layouts to a Campaign",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assigned",
      "item": [
        {
          "id": "b2531093-b668-48b1-8274-a215eb569cba",
          "name": "WidgetAudioDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/:widgetId/audio"
              ],
              "variable": [
                {
                  "id": "widgetId",
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
            "description": "Delete assigned audio widget from specified widget ID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f73fe213-1bb1-45c4-8ef9-7f424b7a014e"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "74209a80-091b-438a-aaf5-1ab7f6b4a0ac",
          "name": "campaignAssignLayout",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "campaign/layout/assign/:campaignId"
              ],
              "variable": [
                {
                  "id": "campaignId",
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
                  "key": "layoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Array of Layout ID/Display Orders to Assign"
                },
                {
                  "key": "unassignLayoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Array of Layout ID/Display Orders to unassign"
                }
              ]
            },
            "description": "Assign Layouts to a Campaign"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6810456c-191e-4170-bf69-20a1c0d12bd6"
            }
          ]
        },
        {
          "id": "e8b74949-9d42-4ac9-acf8-f79bb69c5388",
          "name": "displayGroupDisplayAssign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/display/assign"
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
                  "key": "displayId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Display Ids to assign"
                },
                {
                  "key": "unassignDisplayId",
                  "value": "{}",
                  "disabled": false,
                  "description": "An optional array of Display IDs to unassign"
                }
              ]
            },
            "description": "Adds the provided Displays to the Display Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3dcfb8cb-7fe4-44f5-8457-3a7172fafa33"
            }
          ]
        },
        {
          "id": "a1ef9fd6-ebf5-4576-be8e-cde60e39d2dd",
          "name": "displayGroupDisplayGroupAssign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/displayGroup/assign"
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
                  "key": "unassignDisplayGroupId",
                  "value": "{}",
                  "disabled": false,
                  "description": "An optional array of displayGroup IDs to unassign"
                }
              ]
            },
            "description": "Adds the provided DisplayGroups to the Display Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3f88a4b6-00eb-49a9-a3cb-e2bd1980bd22"
            }
          ]
        },
        {
          "id": "6b083028-a8d5-482d-8bc4-c828f9a051ba",
          "name": "displayGroupMediaAssign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/media/assign"
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
                  "key": "mediaId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Media Ids to assign"
                },
                {
                  "key": "unassignMediaId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional array of Media Id to unassign"
                }
              ]
            },
            "description": "Adds the provided Media to the Display Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0664002c-3a3b-45f9-bd8e-73172ac22bba"
            }
          ]
        },
        {
          "id": "31e8bac2-d91c-49a2-b2c0-60a6db90ea75",
          "name": "displayGroupLayoutsAssign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/layout/assign"
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
                  "key": "layoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Layouts Ids to assign"
                },
                {
                  "key": "unassignLayoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional array of Layouts Id to unassign"
                }
              ]
            },
            "description": "Adds the provided Layouts to the Display Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "969e4bdb-a852-4f4d-8d9c-247e82ce573b"
            }
          ]
        },
        {
          "id": "15f471ba-0b88-4aed-962d-6513dc72d681",
          "name": "playlistLibraryAssign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/library/assign/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
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
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional duration for all Media in this assignment to use on the Widget"
                },
                {
                  "key": "media",
                  "value": "{}",
                  "disabled": false,
                  "description": "Array of Media IDs to assign"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional flag indicating whether to enable the useDuration field"
                }
              ]
            },
            "description": "Assign Media from the Library to this Playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0aeb969-31a0-4bda-aefa-2a61baaada15"
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