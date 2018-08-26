{
  "info": {
    "name": "Xibo API Retrieve User Preferences",
    "_postman_id": "a4d19372-79f9-45bf-810d-3a989ec8c2ba",
    "description": "User preferences for non-state information, such as Layout designer zoom levels",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Retrieve",
      "item": [
        {
          "id": "a30627ec-6732-46e5-b8d6-37bea787400b",
          "name": "userPrefGet",
          "request": {
            "url": "{{default}}/user/pref",
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
            "description": "User preferences for non-state information, such as Layout designer zoom levels"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ae3f535b-ed5a-4009-bfa0-ce6e1383da79"
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