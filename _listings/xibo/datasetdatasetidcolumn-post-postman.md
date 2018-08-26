{
  "info": {
    "name": "Xibo API Add Column",
    "_postman_id": "f8a12ec8-0ae4-46bc-bee4-367e7b92d7d3",
    "description": "Add a Column to a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Column",
      "item": [
        {
          "id": "e6292384-6794-4e0a-a28e-203c614106ba",
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
              "id": "9a3a44c4-3ace-425d-907c-c2372c20d033"
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