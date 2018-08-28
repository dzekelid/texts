{
  "info": {
    "name": "Datumbox Extracts the clear text from Webpage",
    "_postman_id": "50bbae4c-76f5-4b68-a49c-20d715f6eb2d",
    "description": "The Text Extraction function enables you to extract the important information from a given webpage. Extracting the clear text of the documents is an important step before any other analysis.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Adult Content",
      "item": [
        {
          "id": "bb013e6c-2290-4233-8fca-efa9b44b19d3",
          "name": "AdultContentDetection",
          "request": {
            "url": "http://api.datumbox.com/1.0/AdultContentDetection.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Adult Content Detection function classifies the documents as adult or noadult based on their context. It can be used to detect whether a document contains content unsuitable for minors."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8f70a89e-476d-4837-85bb-bb107fd6525d"
            }
          ]
        }
      ]
    },
    {
      "name": "Commercial",
      "item": [
        {
          "id": "397cd420-0e7b-47b1-9273-6b7bf77fefff",
          "name": "CommercialDetection",
          "request": {
            "url": "http://api.datumbox.com/1.0/CommercialDetection.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Commercial Detection function labels the documents as commercial or non-commercial based on their keywords and expressions. It can be used to detect whether a website is commercial or not."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2ace3983-ac78-4f64-9cea-4532de09aa80"
            }
          ]
        }
      ]
    },
    {
      "name": "DocumentsSimilarity",
      "item": [
        {
          "id": "2350f629-fae9-4c89-ac81-c842b6835125",
          "name": "DocumentSimilarity",
          "request": {
            "url": "http://api.datumbox.com/1.0/DocumentSimilarity.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "copy",
                  "value": "{}",
                  "disabled": false,
                  "description": "The second text"
                },
                {
                  "key": "original",
                  "value": "{}",
                  "disabled": false,
                  "description": "The first text"
                }
              ]
            },
            "description": "The Document Similarity function estimates the degree of similarity between two documents. It can be used to detect duplicate webpages or detect plagiarism."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b06fdfd1-2f4c-4a0d-a284-ac05d30b2fe0"
            }
          ]
        }
      ]
    },
    {
      "name": "Educational",
      "item": [
        {
          "id": "0bec4c48-534e-4924-9da9-6a91bf7d1210",
          "name": "EducationalDetection",
          "request": {
            "url": "http://api.datumbox.com/1.0/EducationalDetection.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Educational Detection function classifies the documents as educational or non-educational based on their context. It can be used to detect whether a website is educational or not."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "36be7fcb-8ad3-4b7f-8d34-478a1df0dfd1"
            }
          ]
        }
      ]
    },
    {
      "name": "Gender",
      "item": [
        {
          "id": "82848d9e-9d5a-475e-8626-0796e2973d38",
          "name": "GenderDetection",
          "request": {
            "url": "http://api.datumbox.com/1.0/GenderDetection.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Gender Detection function identifies if a particular document is written-by or targets-to a man or a woman based on the context, the words and the idioms found in the text."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2075a2de-e8cb-445c-b388-3f21d7dfd647"
            }
          ]
        }
      ]
    },
    {
      "name": "Keyword",
      "item": [
        {
          "id": "d49a7411-f1e8-4fe0-b5fa-1757d87acfc3",
          "name": "KeywordExtraction",
          "request": {
            "url": "http://api.datumbox.com/1.0/KeywordExtraction.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "n",
                  "value": "{}",
                  "disabled": false,
                  "description": "The number of keyword combinations (n-grams) that you wish to extract"
                },
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Keyword Extraction function enables you to extract from an arbitrary document all the keywords and word-combinations along with their occurrences in the text."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fdef3a6d-e805-4632-b562-f68cc33878d7"
            }
          ]
        }
      ]
    },
    {
      "name": "Language",
      "item": [
        {
          "id": "60f1d02e-31c8-4b3c-a691-c1f631a0326f",
          "name": "LanguageDetection",
          "request": {
            "url": "http://api.datumbox.com/1.0/LanguageDetection.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Language Detection function identifies the natural language of the given document based on its words and context. This classifier is able to detect 96 different languages."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "29e6cd52-08b0-410d-aabf-79880f40257f"
            }
          ]
        }
      ]
    },
    {
      "name": "Readability",
      "item": [
        {
          "id": "2e524008-381f-4449-8271-4c2207894e11",
          "name": "ReadabilityAssessment",
          "request": {
            "url": "http://api.datumbox.com/1.0/ReadabilityAssessment.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Readability Assessment function determines the degree of readability of a document based on its terms and idioms. The texts are classified as basic, intermediate and advanced depending their difficulty."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dd71309e-7764-4890-a07c-551bd7344eb6"
            }
          ]
        }
      ]
    },
    {
      "name": "Sentiment",
      "item": [
        {
          "id": "85368e70-9634-4f75-bb74-60817d512f9c",
          "name": "SentimentAnalysis",
          "request": {
            "url": "http://api.datumbox.com/1.0/SentimentAnalysis.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Sentiment Analysis function classifies documents as positive, negative or neutral (lack of sentiment) depending on whether they express a positive, negative or neutral opinion."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c93a4e7c-1933-45bb-9a35-92abde75f41b"
            }
          ]
        }
      ]
    },
    {
      "name": "Spam",
      "item": [
        {
          "id": "e7b46420-4984-4a54-8b25-e4167e6b10f8",
          "name": "SpamDetection",
          "request": {
            "url": "http://api.datumbox.com/1.0/SpamDetection.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Spam Detection function labels documents as spam or nospam by taking into account their context. It can be used to filter out spam emails and comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bda69c49-4749-4c6e-a1de-862f9be1c5ec"
            }
          ]
        }
      ]
    },
    {
      "name": "Subjectivity",
      "item": [
        {
          "id": "5e7c59af-6511-4285-b64e-3d754225157c",
          "name": "SubjectivityAnalysis",
          "request": {
            "url": "http://api.datumbox.com/1.0/SubjectivityAnalysis.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text that you want to analyze"
                }
              ]
            },
            "description": "The Subjectivity Analysis function categorizes documents as subjective or objective based on their writing style. Texts that express personal opinions are labeled as subjective and the others as objective."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26219247-e5aa-4878-a0ae-9eaf8edc24cd"
            }
          ]
        }
      ]
    },
    {
      "name": "Text",
      "item": [
        {
          "id": "0656cafa-3f62-41e1-9431-307bd452d13d",
          "name": "TextExtraction",
          "request": {
            "url": "http://api.datumbox.com/1.0/TextExtraction.json",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "The HTML source of the webpage"
                }
              ]
            },
            "description": "The Text Extraction function enables you to extract the important information from a given webpage. Extracting the clear text of the documents is an important step before any other analysis."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "328d20ae-9c63-49eb-add4-9d1ac532dcf2"
            }
          ]
        }
      ]
    }
  ]
}