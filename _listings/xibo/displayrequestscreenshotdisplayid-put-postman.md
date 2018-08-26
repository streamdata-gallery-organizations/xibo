{
  "info": {
    "name": "Xibo API Request Screen Shot",
    "_postman_id": "5bc1368d-6d0b-41d3-9d92-8dc64822953b",
    "description": "Notify the display that the CMS would like a screen shot to be sent.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Request",
      "item": [
        {
          "id": "8ca70af6-8461-440d-a3af-274fc7ab8b4f",
          "name": "displayRequestScreenshot",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "display/requestscreenshot/:displayId"
              ],
              "variable": [
                {
                  "id": "displayId",
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
              "mode": "raw"
            },
            "description": "Notify the display that the CMS would like a screen shot to be sent."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5b9c16a9-9cdd-4be2-9073-935369f86380"
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