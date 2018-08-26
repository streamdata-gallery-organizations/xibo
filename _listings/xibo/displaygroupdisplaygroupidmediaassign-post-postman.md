{
  "info": {
    "name": "Xibo API Assign one or more Media items to a Display Group",
    "_postman_id": "b29cd047-ff16-4a33-b347-06387c0e55f1",
    "description": "Adds the provided Media to the Display Group",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assigned",
      "item": [
        {
          "id": "b7ac3561-edb2-4113-abd9-0b64002dbd0f",
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
              "id": "3d70b7a2-3a75-4d12-9b5e-de121e2cac5a"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "c2601ead-d73a-4329-8146-53005f2b4a84",
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
              "id": "c954d1ce-ae0b-4613-86b0-55d85f441177"
            }
          ]
        },
        {
          "id": "6d1e8d36-4690-4289-b24a-2446f2cb033f",
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
              "id": "21fd95bf-d1cb-4467-a6cf-f64418852f2b"
            }
          ]
        },
        {
          "id": "e0980e1d-36d7-4f5b-89fe-f0b3429d3440",
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
              "id": "dc03e6ba-153e-4859-a974-9a72a589a4c9"
            }
          ]
        },
        {
          "id": "8f24d7f4-0a5b-471d-9e67-cfaff289dd18",
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
              "id": "e5c3dc13-dc89-4cda-b03d-2ed9ca1a2317"
            }
          ]
        },
        {
          "id": "b12fb7bb-f08c-4230-a5e1-35c618813f14",
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
              "id": "d3f62219-5f63-4354-a83c-89bd538c455f"
            }
          ]
        },
        {
          "id": "e7a21c36-35df-4f0b-a581-24f16522e9f4",
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
              "id": "c1bc760b-b0aa-4aa6-ac07-d5d922464407"
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