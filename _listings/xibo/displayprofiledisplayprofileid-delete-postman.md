{
  "info": {
    "name": "Xibo API Delete Display Profile",
    "_postman_id": "187782d6-55ff-43e3-b78e-374f92ed27a1",
    "description": "Delete an existing Display Profile",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Display",
      "item": [
        {
          "id": "6680ba8b-5ba9-4622-bc4d-f398aa96807a",
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
              "id": "ab8509e4-e1e3-4dfe-8682-a64f4d924815"
            }
          ]
        },
        {
          "id": "d4aec742-e5a7-4caf-9dc3-c21ddccbb3ef",
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
              "id": "f3ad9242-90d9-43e5-8471-cea778a5e5d6"
            }
          ]
        },
        {
          "id": "236bb0be-a577-442b-833b-cea373980f65",
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
              "id": "c4cbdc9b-4788-4fdf-9d95-1606e3b8e128"
            }
          ]
        },
        {
          "id": "4a58745d-70aa-41b0-857b-2d162118c2b7",
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
              "id": "e8027b7e-e5b7-4768-b4e9-cc864bad2ce8"
            }
          ]
        },
        {
          "id": "078bd7b3-3ebb-4963-b258-8f22ba38a025",
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
              "id": "d17cc792-5592-484f-86a2-6fa9f8c00690"
            }
          ]
        },
        {
          "id": "9d82e866-0127-4dd8-9ee0-ca04fe422d8e",
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
              "id": "bcc0eba1-de21-41fe-a54e-9e3ffc14bcfb"
            }
          ]
        },
        {
          "id": "a39414a7-395b-4bd6-9bb2-f5f073f4c659",
          "name": "displayProfileSearch",
          "request": {
            "url": "{{default}}/displayprofile",
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
            "description": "Search this users Display Profiles"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e50ba80-7358-470c-9947-d59a4b2b32ef"
            }
          ]
        },
        {
          "id": "2c3a4d4c-d59b-4ec0-a839-c9234942ae9c",
          "name": "displayProfileAdd",
          "request": {
            "url": "{{default}}/displayprofile",
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
                  "key": "isDefault",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating if this is the default profile for the client type"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Name of the Display Profile"
                },
                {
                  "key": "type",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Client Type this Profile will apply to"
                }
              ]
            },
            "description": "Add a Display Profile"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cc29eb69-17d9-446b-84eb-9d39bdf093bc"
            }
          ]
        },
        {
          "id": "3c8bce53-5516-40a9-81f1-aa53b285aa5c",
          "name": "displayProfileDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displayprofile/:displayProfileId"
              ],
              "variable": [
                {
                  "id": "displayProfileId",
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
            "description": "Delete an existing Display Profile"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "915f2718-7492-4a07-911f-7790750a0e53"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "d1278eea-2619-404f-a100-90ec367cd3f9",
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
              "id": "3f74a362-012d-49ba-875f-d30afa8bf908"
            }
          ]
        },
        {
          "id": "f60b27e5-4ecf-4a01-87e1-978527104ddf",
          "name": "displayProfileEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displayprofile/:displayProfileId"
              ],
              "variable": [
                {
                  "id": "displayProfileId",
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
                  "key": "isDefault",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating if this is the default profile for the client type"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Name of the Display Profile"
                },
                {
                  "key": "type",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Client Type this Profile will apply to"
                }
              ]
            },
            "description": "Edit a Display Profile"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "94ad2ad2-73b9-4ea5-a4cb-ed37857fa5ed"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "81e09a3a-fcc2-4e82-8832-15e4d93a7345",
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
              "id": "c352fade-62ff-4621-8921-9a679e837f5a"
            }
          ]
        },
        {
          "id": "8bd1fe18-8135-439e-a83b-18bcb826afef",
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
              "id": "05bfd95e-4951-4669-a6bc-1919a67c4cac"
            }
          ]
        },
        {
          "id": "45894b3e-a881-41b3-a03d-322a2644e461",
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
              "id": "25414a84-6a7d-4536-8361-1961907dfb4b"
            }
          ]
        },
        {
          "id": "17b3289a-3cdb-413f-ba89-878b970fe7da",
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
              "id": "8e46a76e-8fc4-4cf9-9984-68a6204fc622"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassigns",
      "item": [
        {
          "id": "2c224959-3f74-441d-b3b2-c7733aa39a1f",
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
              "id": "91d08fd1-7fc7-4956-861a-613880b15de2"
            }
          ]
        },
        {
          "id": "d74bb143-1716-4e30-9b89-03f3fb71ade3",
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
              "id": "c0b7c975-d666-4659-86c5-2e408c435634"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassign",
      "item": [
        {
          "id": "92eab398-90ae-4a31-8113-c5484dee628f",
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
              "id": "d6505e66-f6c9-4c90-b77f-b598b07a2dc4"
            }
          ]
        },
        {
          "id": "c087c328-ccb9-4955-87e8-12eb3fb74c20",
          "name": "displayGroupLayoutUnassign",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/layout/unassign"
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
                  "description": "The Layout Ids to unassign"
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
              "id": "850e7894-4a4d-4211-8599-96c55a52d709"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "c661e3d2-a343-44b7-8d20-d060e8334c69",
          "name": "displayGroupDisplayVersion",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/version"
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
                  "description": "The Media Id of the Installer File"
                }
              ]
            },
            "description": "Sets the version instructions on all Displays in the Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "607fd55f-d701-43dc-b745-a716dee6706f"
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