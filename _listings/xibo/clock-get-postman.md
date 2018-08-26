{
  "info": {
    "name": "Xibo API The current CMS time",
    "_postman_id": "2653e6c6-c723-4deb-861a-5a230ce15a8a",
    "description": "The Time",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "The",
      "item": [
        {
          "id": "5c366299-286e-42e0-8aa0-3b7512bd8553",
          "name": "clock",
          "request": {
            "url": "{{default}}/clock",
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
            "description": "The Time"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5070eab3-cb0b-4ebe-b9dd-3a17976d34fe"
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