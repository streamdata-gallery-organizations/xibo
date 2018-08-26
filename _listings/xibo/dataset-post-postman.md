{
  "info": {
    "name": "Xibo API Add DataSet",
    "_postman_id": "60b8f25c-7e6e-4216-b268-b9c4e9ba02e0",
    "description": "Add a DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "DataSet",
      "item": [
        {
          "id": "a1dbed51-e87a-4fe8-89f4-804432e8c01f",
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
              "id": "2f3be8eb-c57c-45cd-895e-b279596cc6c9"
            }
          ]
        },
        {
          "id": "b0cb0453-26b6-4176-84ab-a3a6e49874a6",
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
              "id": "fbaa5c7d-4210-4a2e-9ee6-4b3db49ec58d"
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