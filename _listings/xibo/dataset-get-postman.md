{
  "info": {
    "name": "Xibo API DataSet Search",
    "_postman_id": "77fb6054-9bcc-4ca2-aedc-54c2658fad86",
    "description": "Search this users DataSets",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "DataSet",
      "item": [
        {
          "id": "cfa521bf-212e-4ddb-bc94-ac570059e47a",
          "name": "dataSetSearch",
          "request": {
            "url": "{{default}}/dataset",
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
            "description": "Search this users DataSets"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2d795b4a-e8ca-4046-8de6-f994c0ec12f8"
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