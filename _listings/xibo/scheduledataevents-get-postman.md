{
  "info": {
    "name": "Xibo API Generates the calendar that we draw events on",
    "_postman_id": "7f31e49f-c5aa-42d1-b0be-12d1476e0ad4",
    "description": "",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Generates",
      "item": [
        {
          "id": "164eb311-15b8-4c70-b26b-c1bb15c4f203",
          "name": "scheduleCalendarData",
          "request": {
            "url": "{{default}}/schedule/data/events",
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
            "description": "Generates the calendar that we draw events on"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fc92af3a-dead-43e5-835d-522305788de1"
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