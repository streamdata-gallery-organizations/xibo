{
  "info": {
    "name": "Xibo API Add a template from a Layout",
    "_postman_id": "5f140c68-6c54-4356-8e55-a97558fc5c66",
    "description": "Use the provided layout as a base for a new template",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Unassign",
      "item": [
        {
          "id": "b8f6bcb3-e019-40d2-bc2b-c523c09e1a5a",
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
              "id": "d3c3094f-b67d-4e0e-a40b-99865efe68b5"
            }
          ]
        },
        {
          "id": "4c40a274-2607-4852-867c-cf17a96e255c",
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
              "id": "097019bb-3848-41fa-9f8e-91a098d713e8"
            }
          ]
        }
      ]
    },
    {
      "name": "Template",
      "item": [
        {
          "id": "a64f242e-b443-4ed3-9389-cecd40915131",
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
              "id": "5094f7d4-ac28-461c-aead-f702b3ff1b50"
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