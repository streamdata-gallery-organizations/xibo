{
  "info": {
    "name": "Xibo API Parameters for editing existing image on a layout",
    "_postman_id": "21bdb1e2-4d0d-4c9a-9d78-b02cceff353a",
    "description": "Parameters for editing existing image on a layout, for adding new images, please refer to POST /library documentation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "f6930342-8dce-445a-b41f-3e360a581902",
          "name": "WidgetAudioEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/audio/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "playlistId",
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
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - The Widget Duration"
                },
                {
                  "key": "loop",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the audio loop (only for duration > 0 )?"
                },
                {
                  "key": "mute",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the audio be muted?"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - The Widget name"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - (0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Parameters for editing existing audio widget on a layout, for adding new audio, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ebfe89ea-2786-4eef-9e04-83be7e63a43a"
            }
          ]
        },
        {
          "id": "b3794f52-7f6a-4d71-9d83-22004e54d11d",
          "name": "WidgetImageEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/image/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "playlistId",
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
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "alignId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Horizontal alignment - left, center, bottom"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - The Widget Duration"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Optional Widget Name"
                },
                {
                  "key": "scaleTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Select scale type available options: center, stretch"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only (0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "valignId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Vertical alignment - top, middle, bottom"
                }
              ]
            },
            "description": "Parameters for editing existing image on a layout, for adding new images, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5e7d4749-8e92-4c32-b156-e5665f2a0a69"
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