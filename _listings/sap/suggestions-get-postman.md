{
  "info": {
    "name": "SAP Translation Hub The suggestion resource enables you to get suggestions for short texts during the development process.",
    "_postman_id": "340f79ae-88cb-4b10-9c00-b29f63a59f93",
    "description": "Provides suggestions for short texts based on complete or partial texts and their translations. You can, for example, use the suggestion resource to propose texts while you type texts in a development environment. The texts that the resource proposes are already available in additional languages in the multilingual text repository (MLTR).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "SAP",
      "item": [
        {
          "id": "e9441501-bc38-4355-ba23-cac953e22303",
          "name": "sap-product-terminology-is-organized-by-domains-domains-are-used-in-the-translation-process-to-deter",
          "request": {
            "url": "http://sandbox.api.sap.com/translationhub/api/v1/domains?onlyGroups=%7B%7D&search=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "Specifies the nature of the data in the body so that the receiving agent can process the data accordingly",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "SAP product terminology is organized by domains. Domains are used in the translation process to determine the correct terminology for a given application. <br> This resource returns a list of the domains and domain groups that are available in SAP Translation Hub.<br> You can combine the domain resource with the translation resource to more accurately reflect the subject area of your texts."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "edf19394-2d81-464d-9e4e-000cf3525254"
            }
          ]
        }
      ]
    },
    {
      "name": "Languages",
      "item": [
        {
          "id": "0cc1e2c2-3e2e-4d01-86c7-fb18b3174eee",
          "name": "returns-a-list-of-the-languages-that-sap-translation-hub-supports-you-can-also-check-whether-a-parti",
          "request": {
            "url": "http://sandbox.api.sap.com/translationhub/api/v1/languages?search=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "Specifies the nature of the data in the body so that the receiving agent can process the data accordingly",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the languages that SAP Translation Hub supports. You can also check whether a particualr language is available in SAP Translation Hub."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "38a3bfae-e867-4530-80d6-6ed82d789b9c"
            }
          ]
        }
      ]
    },
    {
      "name": "The",
      "item": [
        {
          "id": "1ccd8527-6287-4a90-aa9d-0fe1a149b66e",
          "name": "provides-suggestions-for-short-texts-based-on-complete-or-partial-texts-and-their-translations-you-c",
          "request": {
            "url": "http://sandbox.api.sap.com/translationhub/api/v1/suggestions?domain=%7B%7D&language=%7B%7D&maxLength=%7B%7D&search=%7B%7D&searchLanguage=%7B%7D&texttype=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "Specifies the nature of the data in the body so that the receiving agent can process the data accordingly",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Provides suggestions for short texts based on complete or partial texts and their translations. You can, for example, use the suggestion resource to propose texts while you type texts in a development environment. The texts that the resource proposes are already available in additional languages in the multilingual text repository (MLTR)."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "1bdcacbd-f5eb-49ea-9eee-17679096b683"
            }
          ]
        }
      ]
    }
  ]
}