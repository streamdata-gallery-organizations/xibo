{
  "info": {
    "name": "Xibo API Delete Row",
    "_postman_id": "c4bff623-47f8-4663-b3ea-21c89c920724",
    "description": "Delete a row of Data to a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Row",
      "item": [
        {
          "id": "2e84ea21-367a-4004-a191-50ad150b1ea8",
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
              "id": "d4499753-6405-4fe4-970a-3d3e3db77271"
            }
          ]
        },
        {
          "id": "d154573c-efa8-4089-8b5b-21ee321c3860",
          "name": "dataSetDataDelete",
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
            "description": "Delete a row of Data to a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "01c9a809-dd8f-443b-ad7f-92399d5bba12"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "5f23ebaf-b76c-4557-8b2e-82338d3443c8",
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
              "id": "b39fef0b-6821-4640-aa4e-0e140db3cc2e"
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