{
  "info": {
    "name": "Xibo API Edit Layout",
    "_postman_id": "bfb9fad6-9cac-45c7-a645-6777336dc1db",
    "description": "Edit a Layout",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assign",
      "item": [
        {
          "id": "debec16f-df90-42c8-ac11-38abc3ea7ad1",
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
              "id": "433ec5f5-d1a9-45f0-9045-6b8abd2c1add"
            }
          ]
        },
        {
          "id": "a7f0e217-61c6-4f23-97f0-33242e3847c5",
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
              "id": "6b89e75e-75e3-4ad2-88cc-753a9b08a9dc"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "b1471cda-4d8b-496a-abda-31c13f92905a",
          "name": "layoutSearch",
          "request": {
            "url": "{{default}}/layout",
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
            "description": "Search for Layouts viewable by this user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8be1b800-0c1e-4df8-a3c2-db5b7a54fe5e"
            }
          ]
        }
      ]
    },
    {
      "name": "Layout",
      "item": [
        {
          "id": "9c45b3b6-940f-44b2-b959-f51ddcc05102",
          "name": "layoutAdd",
          "request": {
            "url": "{{default}}/layout",
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
                  "description": "The layout description"
                },
                {
                  "key": "layoutId",
                  "value": "{}",
                  "disabled": false,
                  "description": "If the Layout should be created with a Template, provide the ID, otherwise dont provide"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The layout name"
                },
                {
                  "key": "resolutionId",
                  "value": "{}",
                  "disabled": false,
                  "description": "If a Template is not provided, provide the resolutionId for this Layout"
                }
              ]
            },
            "description": "Add a new Layout to the CMS"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "af3636e6-1ba5-4e78-93a8-2e54d714b2cf"
            }
          ]
        },
        {
          "id": "ac53a3ef-2d91-4e1f-8f1b-244477080f90",
          "name": "layoutDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/:layoutId"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
            "description": "Delete a Layout"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59b40c6d-bc6f-45e5-8456-1ec1a9b8e4c4"
            }
          ]
        },
        {
          "id": "7acb0a61-0be0-416c-9c06-e154d392e75b",
          "name": "layoutStatus",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/status/:layoutId"
              ],
              "variable": [
                {
                  "id": "layoutId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "Calculate the Layout status and return a Layout"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d12f9fc1-6a7a-481e-841e-5f4d6c583097"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "ddc72108-ca7e-4e94-ade5-ecf823c023f4",
          "name": "displayDefaultLayout",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "display/defaultlayout/:displayId"
              ],
              "variable": [
                {
                  "id": "displayId",
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
                  "description": "The Layout ID"
                }
              ]
            },
            "description": "Sent the default Layout on this Display"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dcf58eb7-b38f-4af9-9b63-5aeb01c3502d"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassign",
      "item": [
        {
          "id": "2c518fd3-7b28-4466-9ab3-7525935fccc8",
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
              "id": "c7cb502c-2c80-4cfb-967d-a129941cfca1"
            }
          ]
        }
      ]
    },
    {
      "name": "Action:",
      "item": [
        {
          "id": "9d01579f-dda7-4012-8b21-08043b95ab01",
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
              "id": "d2b661cc-88a2-4c59-917f-190e7a9bcbae"
            }
          ]
        },
        {
          "id": "1465a1bc-eb2c-43b9-ae48-8b4053969c43",
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
              "id": "2c1b4183-231c-4556-8629-7fd3218cf31a"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "7eca1a79-869d-4fc3-8bc1-b7ea0bf13cde",
          "name": "layoutEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/:layoutId"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
                  "key": "backgroundColor",
                  "value": "{}",
                  "disabled": false,
                  "description": "A HEX color to use as the background color of this Layout"
                },
                {
                  "key": "backgroundImageId",
                  "value": "{}",
                  "disabled": false,
                  "description": "A media ID to use as the background image for this Layout"
                },
                {
                  "key": "backgroundzIndex",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Layer Number to use for the background"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Layout Description"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Layout Name"
                },
                {
                  "key": "resolutionId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Resolution ID to use on this Layout"
                },
                {
                  "key": "retired",
                  "value": "{}",
                  "disabled": false,
                  "description": "A flag indicating whether this Layout is retired"
                },
                {
                  "key": "tags",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of Tags"
                }
              ]
            },
            "description": "Edit a Layout"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "96d397e1-eecf-4040-bf5a-6668fae173b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Retire",
      "item": [
        {
          "id": "722e40b8-a4a0-4456-83fa-517ac1874fd7",
          "name": "layoutRetire",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/retire/:layoutId"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
              "mode": "raw"
            },
            "description": "Retire a Layout so that it isn't available to Schedule. Existing Layouts will still be played"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f24f19f9-4828-41b6-a7f2-28a0f96abbcc"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "e4355243-b6b2-4075-a548-ad847cc682fa",
          "name": "layoutCopy",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/copy/:layoutId"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
                  "key": "copyMediaFiles",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether to make new Copies of all Media Files assigned to the Layout being Copied"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Description for the new Layout"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The name for the new Layout"
                }
              ]
            },
            "description": "Copy a Layout, providing a new name if applicable"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1069204e-5e72-4873-9399-6db0a6f493cd"
            }
          ]
        }
      ]
    },
    {
      "name": "Tag",
      "item": [
        {
          "id": "538d8cd9-bf76-4c5f-9d04-5d3c787f2399",
          "name": "layoutTag",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/:layoutId/tag"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
                  "key": "tag",
                  "value": "{}",
                  "disabled": false,
                  "description": "An array of tags"
                }
              ]
            },
            "description": "Tag a Layout with one or more tags"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fbb9cc65-6609-4619-88d9-44deab247001"
            }
          ]
        }
      ]
    },
    {
      "name": "Untag",
      "item": [
        {
          "id": "5c441f8f-223b-4d28-b4cb-7c66f4e3d757",
          "name": "layoutUntag",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/:layoutId/untag"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
                  "key": "tag",
                  "value": "{}",
                  "disabled": false,
                  "description": "An array of tags"
                }
              ]
            },
            "description": "Untag a Layout with one or more tags"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "838ba638-0e3c-482f-b8f0-298b76c4344e"
            }
          ]
        }
      ]
    },
    {
      "name": "Template",
      "item": [
        {
          "id": "86bb20da-f898-4622-96fa-cdbf27abf7ba",
          "name": "template.add.from.layout",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "template/:layoutId"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "A description of the Template"
                },
                {
                  "key": "includeWidgets",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether to include the widgets in the Template"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Template Name"
                },
                {
                  "key": "tags",
                  "value": "{}",
                  "disabled": false,
                  "description": "Comma separated list of Tags for the template"
                }
              ]
            },
            "description": "Use the provided layout as a base for a new template"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "320354f2-663a-41bc-82b9-e8541d601980"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "0b2b9bc6-e607-43b1-b30b-8f7fea48d661",
          "name": "WidgetAudioEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/audio/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "playlistId",
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
                  "description": "Edit Only - The Widget Duration"
                },
                {
                  "key": "loop",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the audio loop (only for duration > 0 )?"
                },
                {
                  "key": "mute",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the audio be muted?"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - The Widget name"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - (0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Parameters for editing existing audio widget on a layout, for adding new audio, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d43a6445-99a8-4775-8e43-173d229a2bc3"
            }
          ]
        },
        {
          "id": "3d11550d-dd0e-4794-b534-526404fdd848",
          "name": "WidgetImageEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/image/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "playlistId",
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
                  "key": "alignId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Horizontal alignment - left, center, bottom"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - The Widget Duration"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Optional Widget Name"
                },
                {
                  "key": "scaleTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Select scale type available options: center, stretch"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only (0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "valignId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Vertical alignment - top, middle, bottom"
                }
              ]
            },
            "description": "Parameters for editing existing image on a layout, for adding new images, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5e6ebcf9-b557-4dd5-a65f-6d2b2287cff5"
            }
          ]
        },
        {
          "id": "dfc44eba-bc69-4a19-a821-05159e5af500",
          "name": "WidgetPdfEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/pdf/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "playlistId",
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
                  "description": "Edit Only - The Widget Duration"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Optional Widget Name"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Parameters for editing existing pdf on a layout, for adding new files, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f3c01cf4-231d-4b3a-9ce4-c6da51f44e4f"
            }
          ]
        },
        {
          "id": "55f93896-a29b-4efe-a6be-60791a49c489",
          "name": "WidgetVideoEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/video/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "playlistId",
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
                  "description": "Edit Only - The Widget Duration"
                },
                {
                  "key": "loop",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the video loop (only for duration > 0 )?"
                },
                {
                  "key": "mute",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the video be muted?"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Optional Widget Name"
                },
                {
                  "key": "scaleTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "How should the video be scaled, available options: aspect, stretch"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - (0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Parameters for editing existing video on a layout, for adding new videos, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a98577d9-112e-4ba6-b2c3-eeb604d97877"
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