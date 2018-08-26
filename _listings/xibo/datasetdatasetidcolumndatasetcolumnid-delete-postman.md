{
  "info": {
    "name": "Xibo API Delete Column",
    "_postman_id": "d981250a-9ecd-4847-865f-fad9b1b343ad",
    "description": "Delete DataSet Column",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Column",
      "item": [
        {
          "id": "c8b8f926-5862-45eb-9ef7-b274568ca01e",
          "name": "dataSetColumnAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/:dataSetId/column"
              ],
              "variable": [
                {
                  "id": "dataSetId",
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
                  "key": "columnOrder",
                  "value": "{}",
                  "disabled": false,
                  "description": "The display order for this column"
                },
                {
                  "key": "dataSetColumnTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The column type for this column"
                },
                {
                  "key": "dataTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The data type ID for this column"
                },
                {
                  "key": "formula",
                  "value": "{}",
                  "disabled": false,
                  "description": "MySQL SELECT syntax formula for this Column if the column type is formula"
                },
                {
                  "key": "heading",
                  "value": "{}",
                  "disabled": false,
                  "description": "The heading for the Column"
                },
                {
                  "key": "listContent",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of content for drop downs"
                },
                {
                  "key": "remoteField",
                  "value": "{}",
                  "disabled": false,
                  "description": "JSON-String to select Data from the Remote DataSet"
                },
                {
                  "key": "showFilter",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this column should present a filter on DataEntry"
                },
                {
                  "key": "showSort",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this column should allow sorting on DataEntry"
                }
              ]
            },
            "description": "Add a Column to a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "428e3138-b185-484b-b3fe-87d024b87c4f"
            }
          ]
        },
        {
          "id": "518058e0-4605-4827-a21c-3b0a3780414d",
          "name": "dataSetColumnDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/:dataSetId/column/:dataSetColumnId"
              ],
              "variable": [
                {
                  "id": "dataSetColumnId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "dataSetId",
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
            "description": "Delete DataSet Column"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f992a58-2cd1-46dc-bff2-b32c00691a66"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "d814dd9e-5d6e-4a2f-b320-bc3f6971a1d2",
          "name": "dataSetColumnEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/:dataSetId/column/:dataSetColumnId"
              ],
              "variable": [
                {
                  "id": "dataSetColumnId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "dataSetId",
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
                  "key": "columnOrder",
                  "value": "{}",
                  "disabled": false,
                  "description": "The display order for this column"
                },
                {
                  "key": "dataSetColumnTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The column type for this column"
                },
                {
                  "key": "dataTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The data type ID for this column"
                },
                {
                  "key": "formula",
                  "value": "{}",
                  "disabled": false,
                  "description": "MySQL SELECT syntax formula for this Column if the column type is formula"
                },
                {
                  "key": "heading",
                  "value": "{}",
                  "disabled": false,
                  "description": "The heading for the Column"
                },
                {
                  "key": "listContent",
                  "value": "{}",
                  "disabled": false,
                  "description": "A comma separated list of content for drop downs"
                },
                {
                  "key": "remoteField",
                  "value": "{}",
                  "disabled": false,
                  "description": "JSON-String to select Data from the Remote DataSet"
                },
                {
                  "key": "showFilter",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this column should present a filter on DataEntry"
                },
                {
                  "key": "showSort",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this column should allow sorting on DataEntry"
                }
              ]
            },
            "description": "Edit a Column to a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c810c05b-8003-4ef0-bf89-2ec13cbb7bf8"
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