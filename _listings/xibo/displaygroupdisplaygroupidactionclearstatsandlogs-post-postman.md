{
  "info": {
    "name": "Xibo API Action: Clear Stats and Logs",
    "_postman_id": "e9c5695d-73ab-4fe1-aaf2-d2a372e04a02",
    "description": "Clear all stats and logs on this Group",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Action:",
      "item": [
        {
          "id": "929652a0-183f-4ba0-aa44-37425c59456d",
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
              "id": "68db44df-394e-47cc-96af-8b3492f62c79"
            }
          ]
        },
        {
          "id": "77cba436-a84a-4c5d-807f-fca09e8406c2",
          "name": "displayGroupActionClearStatsAndLogs",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/clearStatsAndLogs"
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
            "description": "Clear all stats and logs on this Group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d6f581c1-4271-4753-8134-a1be5b73074e"
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