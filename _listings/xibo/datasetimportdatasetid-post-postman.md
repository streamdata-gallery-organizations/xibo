{
  "info": {
    "name": "Xibo API Import CSV",
    "_postman_id": "f04dcf10-286c-4390-888b-b20349d1bdaa",
    "description": "Import a CSV into a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Import",
      "item": [
        {
          "id": "0fbf40b7-4761-4ef6-96a3-851b0f4383ae",
          "name": "dataSetImport",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/import/:dataSetId"
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
                  "key": "csvImport_{dataSetColumnId}",
                  "value": "{}",
                  "disabled": false,
                  "description": "You need to provide dataSetColumnId after csvImport_, to know your dataSet columns Ids, you will need to use the GET /dataset/{dataSetId}/column call first"
                },
                {
                  "key": "files",
                  "value": "{}",
                  "disabled": false,
                  "description": "The file"
                },
                {
                  "key": "ignorefirstrow",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1), Set to 1 to Ignore first row, useful if the CSV file has headings"
                },
                {
                  "key": "overwrite",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) Set to 1 to erase all content in the dataSet and overwrite it with new content in this import"
                }
              ]
            },
            "description": "Import a CSV into a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d229cccf-c0f8-499f-b144-bacc2ffb2367"
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