---
swagger: "2.0"
x-collection-name: SAP
x-complete: 0
info:
  title: SAP Translation Hub The suggestion resource enables you to get suggestions
    for short texts during the development process.
  description: Provides suggestions for short texts based on complete or partial texts
    and their translations. You can, for example, use the suggestion resource to propose
    texts while you type texts in a development environment. The texts that the resource
    proposes are already available in additional languages in the multilingual text
    repository (MLTR).
  contact:
    name: SAP Translation Hub team
    email: translationhub@sap.com
  version: 1.0.0
host: sandbox.api.sap.com
basePath: /translationhub/api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /suggestions:
    get:
      summary: The suggestion resource enables you to get suggestions for short texts
        during the development process.
      description: Provides suggestions for short texts based on complete or partial
        texts and their translations. You can, for example, use the suggestion resource
        to propose texts while you type texts in a development environment. The texts
        that the resource proposes are already available in additional languages in
        the multilingual text repository (MLTR).
      operationId: provides-suggestions-for-short-texts-based-on-complete-or-partial-texts-and-their-translations-you-c
      x-api-path-slug: suggestions-get
      parameters:
      - in: header
        name: Content-Type
        description: Specifies the nature of the data in the body so that the receiving
          agent can process the data accordingly
      - in: query
        name: domain
        description: Searches for texts in the specified domain(s) or domain group(s)
      - in: query
        name: language
        description: Allows you to search for a text that has translations in the
          specified language(s)
      - in: query
        name: maxLength
        description: Searches for texts up to the specified number of characters
      - in: query
        name: search
        description: Allows you to search for a text in SAP Translation Hub in English
      - in: query
        name: searchLanguage
        description: Allows you to search for a text in any of the languages that
          SAP Translation Hub supports
      - in: query
        name: texttype
        description: Allows you to search for a text that is assigned to one or more
          text types
      responses:
        200:
          description: Successful response
      tags:
      - The
      - Suggestion
      - Resource
      - Enables
      - You
      - To
      - Get
      - Suggestionsshort
      - Texts
      - During
      - Development
      - Process
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---