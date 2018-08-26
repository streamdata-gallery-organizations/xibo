{
  "info": {
    "name": "Xibo API Edit Column",
    "_postman_id": "bb0108b5-83ce-42c1-8739-7c6691a53249",
    "description": "Edit a Column to a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Column",
      "item": [
        {
          "id": "3003009b-f928-4630-88f4-20bee468095f",
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
              "id": "379f927e-cf0d-4e57-a95c-de4de383ec6a"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "5ef965f6-8195-4c7d-adb2-0a1a6ec92486",
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
              "id": "3f1670ec-8516-42d7-9d35-2403eadf4a38"
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