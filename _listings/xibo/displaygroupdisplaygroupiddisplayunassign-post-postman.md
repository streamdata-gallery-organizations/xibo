{
  "info": {
    "name": "Xibo API Unassigns one or more Displays to a Display Group",
    "_postman_id": "18043ccd-b1f3-4538-b1bd-db7e86f6ee59",
    "description": "Removes the provided Displays from the Display Group",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Display",
      "item": [
        {
          "id": "08e9edfa-22e2-4293-8a15-760e11adf087",
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
              "id": "7b87a915-2c20-48c1-8e3e-f92d24548f8a"
            }
          ]
        },
        {
          "id": "6039e2ca-1f76-48aa-8207-22b676db6264",
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
              "id": "75d095b9-5677-4bdd-823d-d9e3ad9168da"
            }
          ]
        },
        {
          "id": "84f0729d-2483-4861-a44c-b87ea1627495",
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
              "id": "489e1091-fb26-4b7b-b663-80569b364875"
            }
          ]
        },
        {
          "id": "19ac0fb0-31a1-4fd3-96ce-76338e9b34fd",
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
              "id": "57744ca9-06f6-4d7e-8191-1a96e4c661fc"
            }
          ]
        },
        {
          "id": "df3832d1-a567-47d3-b4f2-39bc5df2eb9f",
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
              "id": "67c1e1bf-b55d-47cf-9d42-b03f99fdbdc8"
            }
          ]
        },
        {
          "id": "42202cec-004c-43be-82a0-9a0fdb61c373",
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
              "id": "afc4bd43-00c7-4186-8e4d-59b685739ae8"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "5661e749-01db-46b5-a86c-14197592821d",
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
              "id": "3743294e-eae7-4216-a081-514186c888dd"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "25842f6a-a62e-45e7-aba9-2571a86d8b92",
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
              "id": "fb98f7f7-7d61-40aa-85a1-cac20e3fd056"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassigns",
      "item": [
        {
          "id": "ee20cb56-91a0-4e66-8eed-9da3e53339ef",
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
              "id": "48dc5f7b-01b2-4f23-b9b9-84063cf7bcf6"
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