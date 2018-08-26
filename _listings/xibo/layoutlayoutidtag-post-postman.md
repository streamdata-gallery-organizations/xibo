{
  "info": {
    "name": "Xibo API Tag Layout",
    "_postman_id": "9c8fc672-8043-470f-b9a6-b0683db8d0ba",
    "description": "Tag a Layout with one or more tags",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assign",
      "item": [
        {
          "id": "f26de2a1-4291-4783-8dd5-4a580a1943fb",
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
              "id": "f2700329-f2f8-4f96-86a1-ff2ed96a9ab9"
            }
          ]
        },
        {
          "id": "dead1221-a9a6-4a24-8e24-ef154e5a0a10",
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
              "id": "c4b2736b-02c5-4be5-bedb-6094f5eee6e7"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "7b5addd1-ab65-41f6-9320-6b16a0249e0f",
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
              "id": "d414c366-7a9a-4586-9e37-cbe2f33a0255"
            }
          ]
        }
      ]
    },
    {
      "name": "Layout",
      "item": [
        {
          "id": "49538b10-b45a-4630-908b-eefe705ac90c",
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
              "id": "ec38d5d3-a9b0-41b9-bb6f-9583229c4956"
            }
          ]
        },
        {
          "id": "df6fa0d4-3d49-467c-900e-2c9db6561e8d",
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
              "id": "cf04c6d9-1b1c-48c4-bf7c-90ad24a48793"
            }
          ]
        },
        {
          "id": "a250bf9a-b629-40eb-ba67-5ad666f24e98",
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
              "id": "d074e354-efa8-4e72-bc85-7dcb9260886b"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "471b95d8-175f-4e54-a8b6-241152b24e5a",
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
              "id": "e99ec1f6-bf1c-4dd7-b6d7-442fcad6e180"
            }
          ]
        }
      ]
    },
    {
      "name": "Unassign",
      "item": [
        {
          "id": "35ea6ad6-4762-4e4f-beff-ae7ede42cfd3",
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
              "id": "11da3187-660c-482b-a96e-87e7a778e9c8"
            }
          ]
        }
      ]
    },
    {
      "name": "Action:",
      "item": [
        {
          "id": "a3395539-75a4-4cc2-abd0-e070cf1bd1a1",
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
              "id": "103ca55b-869d-4e2a-ba4c-f70c5a35ca9d"
            }
          ]
        },
        {
          "id": "4850af0a-8af3-4abd-9b9a-ecea4c1d75e1",
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
              "id": "c232daaf-d070-4027-bb27-b9e95c50794d"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "b22f8df3-b488-45f9-8e5f-863fb2a9a575",
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
              "id": "04b0dd83-1aa7-43e1-9c90-7f2b139e85fa"
            }
          ]
        }
      ]
    },
    {
      "name": "Retire",
      "item": [
        {
          "id": "2cdf7bcb-3c29-49e9-b497-a4271eda30ed",
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
              "id": "2789ba7f-2459-408b-b20b-5f2a4a54836c"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "63e6a167-2a68-4e62-8a2a-e17ad3551879",
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
              "id": "4cb9feda-49f7-4536-95d6-a3939886eea9"
            }
          ]
        }
      ]
    },
    {
      "name": "Tag",
      "item": [
        {
          "id": "63689ac7-11f4-46a5-a058-bc06c627993a",
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
              "id": "53060bf8-1301-48fe-8cf3-57af8cd01ff4"
            }
          ]
        }
      ]
    },
    {
      "name": "Untag",
      "item": [
        {
          "id": "71ada2c4-998e-44fb-9cb0-7a072f66c77d",
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
              "id": "7c9de7b8-baed-42ef-be52-6dd09ecb58d4"
            }
          ]
        }
      ]
    },
    {
      "name": "Template",
      "item": [
        {
          "id": "d4f0c3b4-1e08-4ac4-b490-698b775bb77b",
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
              "id": "4df5ef81-9e72-4a78-bac4-99b506ab473a"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "4871330a-6125-4a2e-ad01-4c719f50e314",
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
              "id": "f36d8e8a-edcd-42c8-a36e-45f530fc24bd"
            }
          ]
        },
        {
          "id": "b6a31970-7242-4397-ba77-a40a9d7e2f5b",
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
              "id": "5fc1be40-adec-4d39-be8f-1c81dbebe7d5"
            }
          ]
        },
        {
          "id": "cb82cfdb-fa42-4537-969d-c2dab126843e",
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
              "id": "5b07fa5d-5bc4-467c-962c-e2690000ed7a"
            }
          ]
        },
        {
          "id": "297f380a-cd6c-41f2-90b5-cbc2410a2eb4",
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
              "id": "989402fa-ceda-4c19-b4ab-0ffab87e1dca"
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