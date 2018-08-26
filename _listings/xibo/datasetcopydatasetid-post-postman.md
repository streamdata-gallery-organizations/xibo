{
  "info": {
    "name": "Xibo API Copy DataSet",
    "_postman_id": "514595d1-3a37-4532-9843-937bfe93527c",
    "description": "Copy a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Copy",
      "item": [
        {
          "id": "37cd81ef-52cd-43a6-92b8-670670d61dab",
          "name": "dataSetCopy",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/copy/:dataSetId"
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
                  "key": "code",
                  "value": "{}",
                  "disabled": false,
                  "description": "A code for this DataSet"
                },
                {
                  "key": "dataSet",
                  "value": "{}",
                  "disabled": false,
                  "description": "The DataSet Name"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "A description of this DataSet"
                }
              ]
            },
            "description": "Copy a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97dcb914-e9ec-4b36-acd5-6e41b5e924f7"
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