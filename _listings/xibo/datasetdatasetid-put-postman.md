{
  "info": {
    "name": "Xibo API Edit DataSet",
    "_postman_id": "e91b6590-795a-4638-9546-20f66f87324d",
    "description": "Edit a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "DataSet",
      "item": [
        {
          "id": "43bb2351-df84-44fb-9f1b-0939399b5770",
          "name": "dataSetSearch",
          "request": {
            "url": "{{default}}/dataset",
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
            "description": "Search this users DataSets"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0ebecf89-b758-42a2-90d9-eefc066e83f0"
            }
          ]
        },
        {
          "id": "dd3d27f9-1b40-4c5a-b987-afd5085a5ecd",
          "name": "dataSetAdd",
          "request": {
            "url": "{{default}}/dataset",
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
                  "key": "authentication",
                  "value": "{}",
                  "disabled": false,
                  "description": "HTTP Authentication method None|Basic|Digest"
                },
                {
                  "key": "clearRate",
                  "value": "{}",
                  "disabled": false,
                  "description": "How often in seconds should this remote DataSet be truncated"
                },
                {
                  "key": "code",
                  "value": "{}",
                  "disabled": false,
                  "description": "A code for this DataSet"
                },
                {
                  "key": "dataRoot",
                  "value": "{}",
                  "disabled": false,
                  "description": "The root of the data in the Remote source which is used as the base for all remote columns"
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
                },
                {
                  "key": "isRemote",
                  "value": "{}",
                  "disabled": false,
                  "description": "Is this a remote DataSet?"
                },
                {
                  "key": "method",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Request Method GET or POST"
                },
                {
                  "key": "password",
                  "value": "{}",
                  "disabled": false,
                  "description": "HTTP Authentication Password"
                },
                {
                  "key": "postData",
                  "value": "{}",
                  "disabled": false,
                  "description": "query parameter encoded data to add to the request"
                },
                {
                  "key": "refreshRate",
                  "value": "{}",
                  "disabled": false,
                  "description": "How often in seconds should this remote DataSet be refreshed"
                },
                {
                  "key": "runsAfter",
                  "value": "{}",
                  "disabled": false,
                  "description": "An optional dataSetId which should be run before this Remote DataSet"
                },
                {
                  "key": "summarize",
                  "value": "{}",
                  "disabled": false,
                  "description": "Should the data be aggregated? None|Summarize|Count"
                },
                {
                  "key": "summarizeField",
                  "value": "{}",
                  "disabled": false,
                  "description": "Which field should be used to summarize"
                },
                {
                  "key": "uri",
                  "value": "{}",
                  "disabled": false,
                  "description": "The URI, without query parameters"
                },
                {
                  "key": "username",
                  "value": "{}",
                  "disabled": false,
                  "description": "HTTP Authentication User Name"
                }
              ]
            },
            "description": "Add a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "72249b1b-6cd8-4dc5-a328-968f2e6d9bdf"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "4bd79c55-4234-45e9-9aae-f843f0587ff8",
          "name": "dataSetEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/:dataSetId"
              ],
              "variable": [
                {
                  "id": "dataSetId",
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
                  "key": "authentication",
                  "value": "{}",
                  "disabled": false,
                  "description": "HTTP Authentication method None|Basic|Digest"
                },
                {
                  "key": "clearRate",
                  "value": "{}",
                  "disabled": false,
                  "description": "How often in seconds should this remote DataSet be truncated"
                },
                {
                  "key": "code",
                  "value": "{}",
                  "disabled": false,
                  "description": "A code for this DataSet"
                },
                {
                  "key": "dataRoot",
                  "value": "{}",
                  "disabled": false,
                  "description": "The root of the data in the Remote source which is used as the base for all remote columns"
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
                },
                {
                  "key": "isRemote",
                  "value": "{}",
                  "disabled": false,
                  "description": "Is this a remote DataSet?"
                },
                {
                  "key": "method",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Request Method GET or POST"
                },
                {
                  "key": "password",
                  "value": "{}",
                  "disabled": false,
                  "description": "HTTP Authentication Password"
                },
                {
                  "key": "postData",
                  "value": "{}",
                  "disabled": false,
                  "description": "query parameter encoded data to add to the request"
                },
                {
                  "key": "refreshRate",
                  "value": "{}",
                  "disabled": false,
                  "description": "How often in seconds should this remote DataSet be refreshed"
                },
                {
                  "key": "runsAfter",
                  "value": "{}",
                  "disabled": false,
                  "description": "An optional dataSetId which should be run before this Remote DataSet"
                },
                {
                  "key": "summarize",
                  "value": "{}",
                  "disabled": false,
                  "description": "Should the data be aggregated? None|Summarize|Count"
                },
                {
                  "key": "summarizeField",
                  "value": "{}",
                  "disabled": false,
                  "description": "Which field should be used to summarize"
                },
                {
                  "key": "uri",
                  "value": "{}",
                  "disabled": false,
                  "description": "The URI, without query parameters"
                },
                {
                  "key": "username",
                  "value": "{}",
                  "disabled": false,
                  "description": "HTTP Authentication User Name"
                }
              ]
            },
            "description": "Edit a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "92cde2d8-2324-4b82-9490-6edde0a5834d"
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