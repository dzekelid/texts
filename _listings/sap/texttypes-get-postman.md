{
  "info": {
    "name": "SAP Translation Hub Returns a list of the text types available in SAP Translation Hub.",
    "_postman_id": "52547bd7-0520-4cc0-8bee-092d67ef578b",
    "description": "In SAP products, short texts, such as those used on user interfaces (UIs), are characterized by various text types. The type of a specific text is determined by the UI element that it describes. For example,  button texts are described by the text type ```XBUT```. <br> The text type resource returns a list of the text types that are available in SAP Translation Hub. You can combine the '/text type' resource with the '/suggestion' resource to narrow down the results of the suggestion resource.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "SAP",
      "item": [
        {
          "id": "8c0c96a5-09b0-45eb-a674-a1057d6b6756",
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
              "id": "7ef2cbf2-6afe-4278-b6fb-477f9cc8a5c2"
            }
          ]
        }
      ]
    },
    {
      "name": "Languages",
      "item": [
        {
          "id": "3beca876-8294-4459-aced-3d99c40e3b62",
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
              "id": "e37a0f62-4fc8-4733-a9ee-c60ec1eb1890"
            }
          ]
        }
      ]
    },
    {
      "name": "The",
      "item": [
        {
          "id": "dfac19c4-ad23-44dc-b0d5-93696b095001",
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
              "id": "15aec013-8d79-46fc-980d-8a3bb1ee384a"
            }
          ]
        }
      ]
    },
    {
      "name": "Returns",
      "item": [
        {
          "id": "672c9dda-3619-4a6a-adb8-680f6b51cf05",
          "name": "in-sap-products-short-texts-such-as-those-used-on-user-interfaces-uis-are-characterized-by-various-t",
          "request": {
            "url": "http://sandbox.api.sap.com/translationhub/api/v1/texttypes?search=%7B%7D",
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
            "description": "In SAP products, short texts, such as those used on user interfaces (UIs), are characterized by various text types. The type of a specific text is determined by the UI element that it describes. For example,  button texts are described by the text type ```XBUT```. <br> The text type resource returns a list of the text types that are available in SAP Translation Hub. You can combine the '/text type' resource with the '/suggestion' resource to narrow down the results of the suggestion resource."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "b1a67306-6fe4-4f6d-86cb-fc7ac7fc38ac"
            }
          ]
        }
      ]
    }
  ]
}