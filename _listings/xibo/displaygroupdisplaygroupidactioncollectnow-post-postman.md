{
  "info": {
    "name": "Xibo API Action: Collect Now",
    "_postman_id": "bc7cd03b-8291-41c8-a7b4-009811c36baa",
    "description": "Send the collect now action to this DisplayGroup",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Action:",
      "item": [
        {
          "id": "e678266e-559e-48b2-a32a-1deb38b1d2a7",
          "name": "displayGroupActionCollectNow",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/collectNow"
              ],
              "variable": [
                {
                  "id": "displayGroupId",
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
            "description": "Send the collect now action to this DisplayGroup"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56809a67-f9ac-4cfc-afba-b17e39282c9d"
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