{
  "info": {
    "name": "Xibo API Get Library Item Usage Report for Layouts",
    "_postman_id": "33500d00-ccad-4083-bbe2-219f665b3594",
    "description": "Get the records for the library item usage report for Layouts",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Library",
      "item": [
        {
          "id": "614a9cdd-2224-4d84-aa09-976418b8e493",
          "name": "libraryUsageReport",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "library/usage/:mediaId"
              ],
              "variable": [
                {
                  "id": "mediaId",
                  "value": "mediaId",
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
            "description": "Get the records for the library item usage report"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8ad893d0-f9b8-49a0-9a47-9be04827db8a"
            }
          ]
        },
        {
          "id": "6105d9bb-5401-4b86-8c1e-aca166258f50",
          "name": "libraryUsageLayoutsReport",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "library/usage/layouts/:mediaId"
              ],
              "variable": [
                {
                  "id": "mediaId",
                  "value": "mediaId",
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
            "description": "Get the records for the library item usage report for Layouts"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b8dcf95e-836f-4046-824c-b7989f41d05e"
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