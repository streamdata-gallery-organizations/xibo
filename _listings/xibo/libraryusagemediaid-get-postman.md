{
  "info": {
    "name": "Xibo API Get Library Item Usage Report",
    "_postman_id": "267b57db-d473-4db7-8dd6-271b7e14a26f",
    "description": "Get the records for the library item usage report",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Library",
      "item": [
        {
          "id": "6f958428-ae9f-4994-9b57-fd1d08efa02b",
          "name": "libraryUsageReport",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "library/usage/:mediaId"
              ],
              "variable": [
                {
                  "id": "mediaId",
                  "value": "mediaId",
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
            "description": "Get the records for the library item usage report"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f1ebcb46-7e10-48b4-95e9-a812095a78be"
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