{
  "info": {
    "name": "Xibo API Unassign one or more Media items from a Display Group",
    "_postman_id": "b08b84f1-d2be-47b3-b622-7efc1f38c173",
    "description": "Removes the provided from the Display Group",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Display",
      "item": [
        {
          "id": "296dadf1-b84d-45f7-b665-4cf77ba86fa9",
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
              "id": "e3dd1774-0c1c-4445-8054-d87304d740ec"
            }
          ]
        },
        {
          "id": "502ea2b1-7ad3-4cc9-b152-993d88a30426",
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
              "id": "22e4865e-1108-4d7a-b01e-920865c9fa20"
            }
          ]
        },
        {
          "id": "b3b6ab6f-b3a0-43a2-9613-20ecddf22ce5",
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
              "id": "05228d56-3514-4a30-93df-b9d324155bbe"
            }
          ]
        },
        {
          "id": "6bf31fe8-2ed2-4495-8ec5-477682ab187f",
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
              "id": "e8c7cd77-6e02-43f5-b71d-4e89db2e7fc3"
            }
          ]
        },
        {
          "id": "0c7f77ba-9d95-4773-ac55-2f3cb7f50b94",
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
              "id": "7d49dd95-4c5e-45a9-8169-1abe57753a01"
            }
          ]
        },
        {
          "id": "1a44410d-392d-41e2-9577-afcc37de02e0",
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
              "id": "921eb405-ac10-4378-a7d0-90640b4308df"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "0b49b05c-b5a4-4aa3-81c1-b954a8d217d0",
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
              "id": "874f5153-162f-4545-8300-b4f3eb3c89ed"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "c5721a18-9173-4c60-a88d-177992deb0ab",
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
              "id": "e83b081d-6204-4e29-9384-d9ee2a1c6876"
            }
          ]
        },
        {
          "id": "13f36f45-82d9-4524-acd4-a1c42b5b8f3b",
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
              "id": "71d04730-7816-4f1a-b43a-a4cdca03fe28"
            }
          ]
        },
        {
          "id": "ebf71ff6-3aeb-43c7-b7b0-0e5f2cd0fc12",
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
              "id": "6f4ef522-36ed-4c98-b703-5e4beb93589f"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassigns",
      "item": [
        {
          "id": "52bfe061-849f-49cf-b2fe-d1f719a19456",
          "name": "displayGroupDisplayUnassign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/display/unassign"
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
                  "description": "The Display Ids to unassign"
                }
              ]
            },
            "description": "Removes the provided Displays from the Display Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b7252cc0-ce1e-442f-8421-836d6fb8456c"
            }
          ]
        },
        {
          "id": "f1159b06-50db-4c73-a98a-9ebf9873a1b0",
          "name": "displayGroupDisplayGroupUnassign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/displayGroup/unassign"
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
            "description": "Removes the provided DisplayGroups from the Display Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6e56e920-99ef-4662-82b6-1b61a0ed2b4b"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassign",
      "item": [
        {
          "id": "30043bd4-c6f3-4436-b67c-83d93db5a89d",
          "name": "displayGroupMediaUnassign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/media/unassign"
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
                  "description": "The Media Ids to unassign"
                }
              ]
            },
            "description": "Removes the provided from the Display Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aa327845-9daf-4744-acb6-0ee7e61de1cb"
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