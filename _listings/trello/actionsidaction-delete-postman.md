{
  "info": {
    "name": "Trello Delete Actions",
    "_postman_id": "e9c0b215-0b8d-4ae8-9023-8e355e63137c",
    "description": "Delete actions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Actions",
      "item": [
        {
          "id": "9d281f7b-45df-4451-b0b7-6222e23f3a21",
          "name": "deleteActionsByIdAction",
          "request": {
            "url": {
              "protocol": "http",
              "host": "trello.com",
              "path": [
                "1",
                "actions/:idAction"
              ],
              "query": [
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "token",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "idAction",
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
            "description": "Delete actions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b59aeb91-41e9-4b4c-a224-15f6f661782d"
            }
          ]
        }
      ]
    }
  ]
}