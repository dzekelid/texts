---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Update texts
  description: Updates texts for an item in the specified language. The ID of the
    variation and the language code must be specified.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/items/{id}/variations/{variationId}/descriptions:
    get:
      summary: List texts
      description: Lists the texts for an item in all available languages. The ID
        of the variation must be specified.
      operationId: getRestItemsVariationsVariationDescriptions
      x-api-path-slug: restitemsidvariationsvariationiddescriptions-get
      parameters:
      - in: path
        name: id
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - List
      - Texts
    post:
      summary: Create texts
      description: Creates texts for an item. The ID of the variation and the language
        code must be specified.
      operationId: postRestItemsVariationsVariationDescriptions
      x-api-path-slug: restitemsidvariationsvariationiddescriptions-post
      parameters:
      - in: body
        name: /rest/items/{id}/variations/{variationId}/descriptions
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Texts
  /rest/items/{id}/variations/{variationId}/descriptions/{lang}:
    delete:
      summary: Delete texts
      description: Deletes texts for an item in the specified language. The ID of
        the variation and the language code must be specified.
      operationId: deleteRestItemsVariationsVariationDescriptionsLang
      x-api-path-slug: restitemsidvariationsvariationiddescriptionslang-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: lang
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Texts
    get:
      summary: Get texts
      description: Gets the texts for an item in the specified language. The ID of
        the variation and the language code must be specified.
      operationId: getRestItemsVariationsVariationDescriptionsLang
      x-api-path-slug: restitemsidvariationsvariationiddescriptionslang-get
      parameters:
      - in: path
        name: id
      - in: path
        name: lang
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Texts
    put:
      summary: Update texts
      description: Updates texts for an item in the specified language. The ID of
        the variation and the language code must be specified.
      operationId: putRestItemsVariationsVariationDescriptionsLang
      x-api-path-slug: restitemsidvariationsvariationiddescriptionslang-put
      parameters:
      - in: body
        name: /rest/items/{id}/variations/{variationId}/descriptions/{lang}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: path
        name: lang
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Texts
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