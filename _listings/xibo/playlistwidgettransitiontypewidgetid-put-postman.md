{
  "info": {
    "name": "Xibo API Adds In/Out transition",
    "_postman_id": "95ee35f5-e38f-4859-af60-a9944f3d6470",
    "description": "Adds In/Out transition to a specified widget",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "S",
      "item": [
        {
          "id": "98d753db-9e71-49cf-9aaa-e69f66de0754",
          "name": "WidgetEditTransition",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/transition/:type/:widgetId"
              ],
              "variable": [
                {
                  "id": "type",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "widgetId",
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
                  "key": "transitionDirection",
                  "value": "{}",
                  "disabled": false,
                  "description": "The direction for this transition, only appropriate for transitions that move, such as fly"
                },
                {
                  "key": "transitionDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Duration of this transition in milliseconds"
                },
                {
                  "key": "transitionType",
                  "value": "{}",
                  "disabled": false,
                  "description": "Type of a transition, available Options: fly, fadeIn, fadeOut"
                }
              ]
            },
            "description": "Adds In/Out transition to a specified widget"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "435cab80-8e3f-42e5-83b5-6efee1cf5646"
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