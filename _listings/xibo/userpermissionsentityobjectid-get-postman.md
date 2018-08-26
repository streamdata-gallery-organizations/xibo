{
  "info": {
    "name": "Xibo API Permission Data",
    "_postman_id": "01a598a9-ede0-4ca1-b82b-16402f322a0a",
    "description": "Permission data for the Entity and Object Provided.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "DataSet",
      "item": [
        {
          "id": "3edeb8db-7d42-4549-acc1-66fe845efc83",
          "name": "dataSetData",
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
            "description": "Get Data for DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "73cc2608-0c95-4be6-b9ce-0d73b52d2c8c"
            }
          ]
        }
      ]
    },
    {
      "name": "Permission",
      "item": [
        {
          "id": "0aac3fc2-47a0-4bfd-ae25-fc1db41b661b",
          "name": "userPermissionsSearch",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "user/permissions/:entity/:objectId"
              ],
              "variable": [
                {
                  "id": "entity",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "objectId",
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
            "description": "Permission data for the Entity and Object Provided."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e0b3f0cf-c5f4-4344-a1e8-3b8da1d60aea"
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