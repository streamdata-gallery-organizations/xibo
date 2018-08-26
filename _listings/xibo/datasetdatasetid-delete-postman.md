{
  "info": {
    "name": "Xibo API Delete DataSet",
    "_postman_id": "5b4af8ba-075c-4e36-bb3a-fc477db59242",
    "description": "Delete a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "DataSet",
      "item": [
        {
          "id": "fed4f1e0-4238-4ffc-a477-185efbdc4ea5",
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
              "id": "55d782f7-80ef-4896-866b-8b381572debc"
            }
          ]
        },
        {
          "id": "6bc7d59d-0543-460f-88b7-e57f309cf0d9",
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
              "id": "5a8332a3-daf8-4bd3-97a8-4de15035910d"
            }
          ]
        },
        {
          "id": "5c151222-ae02-4548-ac02-863e5adc0dc0",
          "name": "dataSetDelete",
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
            "description": "Delete a DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1995841a-b460-43e0-ae83-59f9d3a7da35"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "5481612e-90f4-4480-9673-6a22d65e67cf",
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
              "id": "6fc8f7fa-2e98-4d33-a963-c55796ee89cb"
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