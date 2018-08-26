{
  "info": {
    "name": "Xibo API DataSet Data",
    "_postman_id": "a6f2285e-e943-4588-b88e-7751554f3f18",
    "description": "Get Data for DataSet",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "DataSet",
      "item": [
        {
          "id": "8dae2fdb-34fc-49df-b5f0-fd47af874067",
          "name": "dataSetData",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "dataset/data/:dataSetId"
              ],
              "variable": [
                {
                  "id": "dataSetId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "Get Data for DataSet"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "342a2ae0-50ab-4945-8b34-fa1aaa9800f3"
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