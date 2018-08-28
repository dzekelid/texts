swagger: "2.0"
x-collection-name: Datumbox
x-complete: 1
info:
  title: DatumBox
  description: datumbox-offers-a-machine-learning-platform-composed-of-14-classifiers-and-natural-language-processing-functions--functions-include-sentiment-analysis-topic-classification-readability-assessment-language-detection-and-much-more-
  version: 1.0.0
host: api.datumbox.com
basePath: 1.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /TextExtraction.json:
    post:
      summary: Extracts the clear text from Webpage
      description: The Text Extraction function enables you to extract the important
        information from a given webpage. Extracting the clear text of the documents
        is an important step before any other analysis.
      operationId: TextExtraction
      x-api-path-slug: textextraction-json-post
      parameters:
      - in: formData
        name: text
        description: The HTML source of the webpage
      responses:
        200:
          description: OK
      tags:
      - Text
      - Extraction