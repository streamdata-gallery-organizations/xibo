{
  "info": {
    "name": "Xibo API Edit Row",
    "_postman_id": "f5c51829-4d64-4831-add2-2ddd16ea1b42",
    "description": "Edit a row of Data to a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Row",
      "item": [
        {
          "id": "d20a0fa2-66c6-4304-9ecb-dd9a27275405",
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
              "id": "dd85b391-a759-4eae-9e4e-f8a9af0820a2"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "eba50158-683a-4516-9c32-2dc43546e16b",
          "name": "dataSetDataEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/data/:dataSetId/:rowId"
              ],
              "variable": [
                {
                  "id": "dataSetId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "rowId",
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
                  "key": "dataSetColumnId_ID",
                  "value": "{}",
                  "disabled": false,
                  "description": "Parameter for each dataSetColumnId in the DataSet"
                }
              ]
            },
            "description": "Edit a row of Data to a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3650628f-874e-4c39-a7cf-c327e30b5ae0"
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