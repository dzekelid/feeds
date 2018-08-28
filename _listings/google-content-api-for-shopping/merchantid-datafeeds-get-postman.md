{
  "info": {
    "name": "Google Content API for Shopping API Get Data Feeds",
    "_postman_id": "91e0c85a-6491-4ac1-acd2-87f35a38686d",
    "description": "Lists the datafeeds in your Merchant Center account. This method can only be called for non-multi-client accounts.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "data",
      "item": [
        {
          "id": "aa79bbea-bece-4459-8e61-8b2cea9086bf",
          "name": "content.datafeeds.list",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.googleapis.com",
              "path": [
                "content",
                "v2",
                ":merchantId/datafeeds"
              ],
              "query": [
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageToken",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "merchantId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the datafeeds in your Merchant Center account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec33040f-d6a4-4398-8623-55b81a0133f1"
            }
          ]
        }
      ]
    }
  ]
}