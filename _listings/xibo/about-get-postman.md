{
  "info": {
    "name": "Xibo API About",
    "_postman_id": "ccbea11d-c051-4050-88d4-fd2c90508c10",
    "description": "Information about this API, such as Version code, etc",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "About",
      "item": [
        {
          "id": "f3fe7b7b-83c1-44fa-ad9c-aead3d89f5b2",
          "name": "about",
          "request": {
            "url": "{{default}}/about",
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
            "description": "Information about this API, such as Version code, etc"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "00a358af-133a-441b-a995-f3feb37b78f7"
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