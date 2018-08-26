{
  "info": {
    "name": "Xibo API Search Columns",
    "_postman_id": "8e75f6da-5a6a-46ee-a3e6-6acfb19d326b",
    "description": "Search Columns for DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Search",
      "item": [
        {
          "id": "59d26997-763a-4478-b0d8-e3ec5576af9a",
          "name": "dataSetColumnSearch",
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
            "description": "Search Columns for DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43114700-51eb-489d-a7aa-a6e58c3dc3a0"
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