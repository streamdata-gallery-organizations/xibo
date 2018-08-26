{
  "info": {
    "name": "Xibo API Add Campaign",
    "_postman_id": "288a6300-4706-4627-a65a-abf7f13a242d",
    "description": "Add a Campaign",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Campaign",
      "item": [
        {
          "id": "615bf3a0-6278-4fae-93fb-cd7284d533d6",
          "name": "campaignAdd",
          "request": {
            "url": "{{default}}/campaign",
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
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name for this Campaign"
                }
              ]
            },
            "description": "Add a Campaign"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca31ff0c-2d24-488e-a6f8-1c55ce848505"
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