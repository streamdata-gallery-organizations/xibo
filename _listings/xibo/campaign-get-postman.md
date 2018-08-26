{
  "info": {
    "name": "Xibo API Search Campaigns",
    "_postman_id": "77f6c6d9-4c71-4d07-b1f8-5ba523d1ada2",
    "description": "Search all Campaigns this user has access to",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Search",
      "item": [
        {
          "id": "95d133dd-1b1f-4c59-8725-fc0ee4dbfb2c",
          "name": "campaignSearch",
          "request": {
            "url": "{{default}}/campaign",
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
            "description": "Search all Campaigns this user has access to"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "04a18d61-3e8c-4ecd-946c-bfeb81fedb01"
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