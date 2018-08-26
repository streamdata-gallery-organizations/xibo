{
  "info": {
    "name": "Xibo API Delete Campaign",
    "_postman_id": "ee5ccaf2-cc62-47c4-ac12-8aa566f37c2f",
    "description": "Delete an existing Campaign",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Campaign",
      "item": [
        {
          "id": "e537b9b9-46bf-42d8-bec9-0ba171edc44e",
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
              "id": "9c27629f-5079-499a-9caf-5178f09e3232"
            }
          ]
        },
        {
          "id": "3ff585cb-1c96-4357-be09-605787c7a00f",
          "name": "campaignDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "campaign/:campaignId"
              ],
              "variable": [
                {
                  "id": "campaignId",
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
            "description": "Delete an existing Campaign"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f0c4a6a4-2df3-47fe-ac34-e7b7971810d5"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "008f9938-165f-4a8c-a928-baabed326d2d",
          "name": "campaignEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "campaign/:campaignId"
              ],
              "variable": [
                {
                  "id": "campaignId",
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
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name for this Campaign"
                }
              ]
            },
            "description": "Edit an existing Campaign"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13e5b2d9-f853-49fa-ab84-35138179aba4"
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