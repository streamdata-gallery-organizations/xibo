{
  "info": {
    "name": "Xibo API Edit Campaign",
    "_postman_id": "cb100677-84be-4c6e-b862-df5bbf7b16ef",
    "description": "Edit an existing Campaign",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Campaign",
      "item": [
        {
          "id": "3e93b82b-9901-4fe5-9e96-d2df30d4b7cc",
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
              "id": "3c977056-a4fc-4e63-8d0d-7604b7c93278"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "3b59c2ff-d57b-47b0-8d3f-be07e935e458",
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
              "id": "f2bd70dd-c800-4253-8cb2-4bacfc1b9e4b"
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