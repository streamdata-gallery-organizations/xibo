{
  "info": {
    "name": "Xibo API Retire Layout",
    "_postman_id": "c2e29d84-51cf-40d6-bfe1-231f9051eb82",
    "description": "Retire a Layout so that it isn't available to Schedule. Existing Layouts will still be played",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assign",
      "item": [
        {
          "id": "f4ee61fc-77ef-4e1e-8d63-d0390cc0f78d",
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
              "id": "4181d42e-a2f8-4e89-9b64-92df7cceb944"
            }
          ]
        },
        {
          "id": "98aaf752-15bd-4cd3-99bb-36577ed75d88",
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
              "id": "22659f91-680f-4b3c-8776-cb10ece0ab0c"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "72420f5b-5fdb-4604-9f49-5ae8cf408489",
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
              "id": "94001318-6575-4408-a03d-127a0a41e07c"
            }
          ]
        }
      ]
    },
    {
      "name": "Layout",
      "item": [
        {
          "id": "08350d25-a702-41bc-a2cc-6555a9649ffd",
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
              "id": "53a61a11-1704-4b6b-8778-361f9c16152f"
            }
          ]
        },
        {
          "id": "829a0e58-f79c-48e2-89c6-df33fdd82121",
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
              "id": "c092bf92-a8aa-4780-b310-d4e0305624e8"
            }
          ]
        },
        {
          "id": "8790e75d-e81b-4184-9ec8-363eb6534996",
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
              "id": "94cc62c4-abc0-4f1a-875a-d41078b3f0ca"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "909de99f-9370-4327-81ff-0d8255e582aa",
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
              "id": "1fcca57c-4865-4f68-9aa9-1c885c949aeb"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassign",
      "item": [
        {
          "id": "6af55014-6757-47c1-a777-0ee873b9f141",
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
              "id": "41478496-5443-41a0-ad95-c3bad5bac739"
            }
          ]
        }
      ]
    },
    {
      "name": "Action:",
      "item": [
        {
          "id": "459ba4fd-5741-4dcb-8cc4-c40bdd7130e2",
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
              "id": "446a5b5f-a7b2-48a8-8d44-cc810ef887b9"
            }
          ]
        },
        {
          "id": "120bb9c0-e279-4d8f-894d-e096007d80fe",
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
              "id": "a0ee0618-06ab-4794-891e-0707bd6f937f"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "d536ee21-b1f5-49b1-8373-2fb6e99d46d5",
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
              "id": "eb8049b9-a9d3-48fa-a3c9-2622b240a1e9"
            }
          ]
        }
      ]
    },
    {
      "name": "Retire",
      "item": [
        {
          "id": "23827553-8894-4ab8-9596-7a19cac24e28",
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
              "id": "73f255ed-5c39-471e-ad0f-c36fd7b37404"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "83cfa2d4-39b1-447a-830f-06b3dc819c23",
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
              "id": "fb8ecbc2-1b24-45fb-bfdc-44213f877953"
            }
          ]
        }
      ]
    },
    {
      "name": "Tag",
      "item": [
        {
          "id": "f4c203ec-0d0d-4027-aeaf-a4336a9e53d9",
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
              "id": "e24bb824-42a7-473b-88e2-181257a3c593"
            }
          ]
        }
      ]
    },
    {
      "name": "Untag",
      "item": [
        {
          "id": "5450892d-9ebe-499f-9a22-ce263b62d1fd",
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
              "id": "96cf74fe-4315-4afa-b206-2b9b8b108ab8"
            }
          ]
        }
      ]
    },
    {
      "name": "Template",
      "item": [
        {
          "id": "ac4d59bc-6bb5-49dd-adbf-3497a30996cb",
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
              "id": "77274e6c-4071-43f8-ad4c-6e8565c3ef99"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "1bf6c090-c72c-48be-9420-a2dff8ac6cb1",
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
              "id": "59712e82-fded-4b18-89d3-9bbcba4d675e"
            }
          ]
        },
        {
          "id": "f437171c-c210-465a-aeeb-0c85c6c92d19",
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
              "id": "0c59b150-b255-4d85-8b56-d33628152cc3"
            }
          ]
        },
        {
          "id": "2c2ffcf8-eb19-4ac3-9d55-4f7e6d36afac",
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
              "id": "73d02ce5-0f5e-4a13-ba5a-09366c2db08a"
            }
          ]
        },
        {
          "id": "215f9a05-0a7a-4eed-b654-f30456bb743c",
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
              "id": "4bfb3e8e-8adf-48a1-b708-c55231f1b272"
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