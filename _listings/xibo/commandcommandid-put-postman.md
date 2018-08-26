{
  "info": {
    "name": "Xibo API Edit Command",
    "_postman_id": "7461d3c5-03bb-4fa6-90ea-2af52338d255",
    "description": "Edit the provided command",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Command",
      "item": [
        {
          "id": "7a374b28-f2a0-4ef4-ada1-fa9de03127ae",
          "name": "commandSearch",
          "request": {
            "url": "{{default}}/command",
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
            "description": "Search this users Commands"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d42c8fea-7afd-4bcc-92d2-b9bf311baea8"
            }
          ]
        },
        {
          "id": "6b988203-0feb-4c3c-9d0a-78318628596b",
          "name": "commandAdd",
          "request": {
            "url": "{{default}}/command",
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
                  "key": "code",
                  "value": "{}",
                  "disabled": false,
                  "description": "A unique code for this command"
                },
                {
                  "key": "command",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Command Name"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "A description for the command"
                }
              ]
            },
            "description": "Add a Command"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c2980151-f6b9-402e-8dac-b7edf5e561ff"
            }
          ]
        },
        {
          "id": "d973562e-a852-4fd4-9355-fa506427b424",
          "name": "commandDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "command/:commandId"
              ],
              "variable": [
                {
                  "id": "commandId",
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
            "description": "Delete the provided command"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2737a920-6abb-4e00-b7e2-125d9ad62ff4"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "bd2746e8-c9a7-465e-9ba8-dcab1734d85d",
          "name": "commandEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "command/:commandId"
              ],
              "variable": [
                {
                  "id": "commandId",
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
                  "key": "command",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Command Name"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "A description for the command"
                }
              ]
            },
            "description": "Edit the provided command"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bdc1846b-6f15-417d-84cb-7078050eb99c"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "814b1d2f-2904-4ee3-8b04-4c1cc5570402",
          "name": "displayGroupActionCommand",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "displaygroup/:displayGroupId/action/command"
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
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "commandId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Command Id"
                }
              ]
            },
            "description": "Send a predefined command to this Group of Displays"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "487f27ee-303d-48bb-82af-fab6af23b2a6"
            }
          ]
        }
      ]
    },
    {
      "name": "Shell",
      "item": [
        {
          "id": "3c1e98a9-4b5f-4fad-8652-0b3ffb4e3a9b",
          "name": "WidgetShellCommandAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/shellCommand/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
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
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "commandCode",
                  "value": "{}",
                  "disabled": false,
                  "description": "Enter a reference code for exiting command in CMS"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Widget Duration"
                },
                {
                  "key": "launchThroughCmd",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) Windows only, Should the player launch this command through the windows command line (cmd"
                },
                {
                  "key": "linuxCommand",
                  "value": "{}",
                  "disabled": false,
                  "description": "Enter a Android / Linux command line compatible command"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "terminateCommand",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) Should the player forcefully terminate the command after the duration specified, 0 to let the command terminate naturally"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "useTaskkill",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) Windows only, should the player use taskkill to terminate commands"
                },
                {
                  "key": "windowsCommand",
                  "value": "{}",
                  "disabled": false,
                  "description": "Enter a Windows command line compatible command"
                }
              ]
            },
            "description": "Add a new Shell Command Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e0f9f5c-58af-4881-9c00-08720ea17136"
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