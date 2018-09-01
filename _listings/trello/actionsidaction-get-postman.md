{
  "info": {
    "name": "Trello Get Actions",
    "_postman_id": "8e1c0296-3aa5-4ff3-8a74-3697291cfc84",
    "description": "Get actions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Actions",
      "item": [
        {
          "id": "d7e69c2b-6bf7-45a6-ba7f-30c4a23a7fce",
          "name": "getActionsByIdAction",
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
                  "key": "display",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "entities",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "member",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "memberCreator",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "memberCreator_fields",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "member_fields",
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
            "description": "Get actions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1fc0ee25-7295-427b-89ac-1bdd6618cdef"
            }
          ]
        },
        {
          "id": "7b0d0be0-ae20-4a49-a564-660dfacc808f",
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
              "id": "21cc420d-2a14-45a2-b3dd-0c9335ae5d25"
            }
          ]
        }
      ]
    }
  ]
}