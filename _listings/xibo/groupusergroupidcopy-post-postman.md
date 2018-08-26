{
  "info": {
    "name": "Xibo API Copy User Group",
    "_postman_id": "60861ea4-df72-4cde-b2fa-e32c9ec8d56d",
    "description": "Copy an user group, optionally copying the group members",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Copy",
      "item": [
        {
          "id": "3aeea938-33fd-4a48-9eaa-917339fb95b0",
          "name": "dataSetCopy",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/copy/:dataSetId"
              ],
              "variable": [
                {
                  "id": "dataSetId",
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
                  "key": "code",
                  "value": "{}",
                  "disabled": false,
                  "description": "A code for this DataSet"
                },
                {
                  "key": "dataSet",
                  "value": "{}",
                  "disabled": false,
                  "description": "The DataSet Name"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "A description of this DataSet"
                }
              ]
            },
            "description": "Copy a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "00658938-7b55-4da7-89c7-3e426e561f8f"
            }
          ]
        },
        {
          "id": "2a7b8081-4620-4aa6-bc28-dd7f339d62f4",
          "name": "layoutCopy",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "layout/copy/:layoutId"
              ],
              "variable": [
                {
                  "id": "layoutId",
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
                  "key": "copyMediaFiles",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether to make new Copies of all Media Files assigned to the Layout being Copied"
                },
                {
                  "key": "description",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Description for the new Layout"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The name for the new Layout"
                }
              ]
            },
            "description": "Copy a Layout, providing a new name if applicable"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30328437-3b42-4116-b755-a61ff4cb2804"
            }
          ]
        },
        {
          "id": "b4f8f5a1-dde3-4276-babb-1f1fe723f434",
          "name": "userGroupCopy",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "group/:userGroupId/copy"
              ],
              "variable": [
                {
                  "id": "userGroupId",
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
                  "key": "copyMembers",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether to copy group members"
                },
                {
                  "key": "group",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Group Name"
                }
              ]
            },
            "description": "Copy an user group, optionally copying the group members"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f547f0d-141e-4122-9c78-be7d927c15e3"
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