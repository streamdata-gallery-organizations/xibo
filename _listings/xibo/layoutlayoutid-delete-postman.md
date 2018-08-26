{
  "info": {
    "name": "Xibo API Delete Layout",
    "_postman_id": "97eadde6-63f0-49d7-b43c-cbb332568630",
    "description": "Delete a Layout",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assign",
      "item": [
        {
          "id": "9fb647e6-8da3-4057-859e-5f38a73dd2c2",
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
              "id": "c53f3270-959e-45a1-b90d-b94f0da75764"
            }
          ]
        },
        {
          "id": "96afa4f8-6c4a-49d7-9865-f7ecfa8d9f2d",
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
              "id": "f8f5513c-74ad-44f5-8f58-ed9cb6dfca3d"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "6b59b801-878e-4aed-9e91-ccd4f3ad98b6",
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
              "id": "9b4b9552-df49-4cf1-aca0-574d0998dbe6"
            }
          ]
        }
      ]
    },
    {
      "name": "Layout",
      "item": [
        {
          "id": "97ee0ad6-9577-4e57-b6f1-b8c801149d8e",
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
              "id": "8e8403e9-b61a-4be1-ad78-97ad30fbc15d"
            }
          ]
        },
        {
          "id": "51da2240-5a03-4d65-9f57-2ad88b454240",
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
              "id": "53071884-fed6-4c30-955d-2f6485a6ba5f"
            }
          ]
        },
        {
          "id": "6d502252-8ef2-4f01-8343-7fba38ed02b7",
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
              "id": "7fc0dd82-0635-423f-a636-ed30a9945f11"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "e6e7be83-e7bc-4de4-ae88-4883cc9ecefa",
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
              "id": "ce0f7b65-fb58-4280-8fef-e9331d9b8b71"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassign",
      "item": [
        {
          "id": "f2d4bbcd-6828-4a84-9efa-67bac35b75a6",
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
              "id": "974d6347-b8eb-4861-8624-cc5ca02e9aa3"
            }
          ]
        }
      ]
    },
    {
      "name": "Action:",
      "item": [
        {
          "id": "bfa53e93-5772-41ff-95d7-e8673f12afed",
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
              "id": "855434aa-efb8-4699-82db-28a383820f13"
            }
          ]
        },
        {
          "id": "47296bd3-b106-4ddd-a91d-a8b635c3db2a",
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
              "id": "8e0bb1fd-010e-49bc-bd69-80eb6f35d365"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "e04024d1-0b08-4a91-a236-89228f8817d3",
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
              "id": "396e97f3-fe34-48bc-bf7b-be905f69f06c"
            }
          ]
        }
      ]
    },
    {
      "name": "Retire",
      "item": [
        {
          "id": "97e8d4a1-3abf-44a8-8099-b113f33c8b1c",
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
              "id": "3fc29be8-92ab-46bb-9854-72fae1898068"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "a8d472e3-a04a-4ada-bd5e-d40c1fff90a0",
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
              "id": "f0d1fe6c-555a-4035-8455-d7c6840ba36f"
            }
          ]
        }
      ]
    },
    {
      "name": "Tag",
      "item": [
        {
          "id": "f6011b55-8bf9-4902-8e29-ae0fbe44c737",
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
              "id": "3fcf6998-01ba-4d17-9279-dceff23ce31c"
            }
          ]
        }
      ]
    },
    {
      "name": "Untag",
      "item": [
        {
          "id": "28d26e80-b8d5-49d2-9409-46dd1a456bc3",
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
              "id": "b5a7a10f-230a-44e4-8ae4-40538072334d"
            }
          ]
        }
      ]
    },
    {
      "name": "Template",
      "item": [
        {
          "id": "a1669dae-83ef-4432-b98a-23bfbc5d2658",
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
              "id": "e1651c35-3308-405b-949c-53642c078e14"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "7bd33fc1-5d20-46c0-9393-97513cfa200d",
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
              "id": "a560e213-c33f-4715-9263-d120aa7f40af"
            }
          ]
        },
        {
          "id": "2a0be497-a6d5-48e7-bb69-59289a2ba3ad",
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
              "id": "ea742d05-2656-4343-ac5a-30275cbaabd4"
            }
          ]
        },
        {
          "id": "9f81c775-2ca5-498f-9649-0193a4d3a9a9",
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
              "id": "3e423ba4-0f1b-4764-9fbe-6fe9598e9584"
            }
          ]
        },
        {
          "id": "4af5b47d-bd59-47af-bf80-959f5e72542f",
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
              "id": "f132158d-0d21-43b7-aa2b-503dc37c0f71"
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