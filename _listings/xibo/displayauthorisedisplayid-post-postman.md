{
  "info": {
    "name": "Xibo API Toggle authorised",
    "_postman_id": "7681bfba-9e68-423b-9645-d04067c59345",
    "description": "Toggle authorised for the Display.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Toggle",
      "item": [
        {
          "id": "6d464705-cf91-428c-9b6c-9c44cc14bb9c",
          "name": "displayToggleAuthorise",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "display/authorise/:displayId"
              ],
              "variable": [
                {
                  "id": "displayId",
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
              "mode": "raw"
            },
            "description": "Toggle authorised for the Display."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e1b6713-fa7f-4f6a-a5f0-b88d9f4888ec"
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