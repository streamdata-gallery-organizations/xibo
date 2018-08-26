{
  "info": {
    "name": "Xibo API Add Row",
    "_postman_id": "a7c5c66f-fa0e-49b7-b370-4f8a6367490a",
    "description": "Add a row of Data to a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Row",
      "item": [
        {
          "id": "7be4e422-b3df-4e72-887f-600cb09e68fe",
          "name": "dataSetDataAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/data/:dataSetId"
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
                  "key": "dataSetColumnId_ID",
                  "value": "{}",
                  "disabled": false,
                  "description": "Parameter for each dataSetColumnId in the DataSet"
                }
              ]
            },
            "description": "Add a row of Data to a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ac500ce8-0bf1-499f-a7a4-24329e21e1ab"
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