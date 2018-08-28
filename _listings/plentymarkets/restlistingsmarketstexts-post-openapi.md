---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Create a listing market text
  description: Creates a listing market text for a given listing market ID. If an
    entry with same data already exists the request will be ignored and the old entry
    will be returned.
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
  /rest/items/{itemId}/variations/{variationId}/variation_properties/{propertyId}/texts:
    get:
      summary: Get property value texts
      description: Gets the texts saved for a specific property of the type Text in
        all available languages. The ID of the property must be specified.
      operationId: getRestItemsItemVariationsVariationVariationPropertiesPropertyTexts
      x-api-path-slug: restitemsitemidvariationsvariationidvariation-propertiespropertyidtexts-get
      parameters:
      - in: path
        name: itemId
      - in: path
        name: propertyId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Property
      - Value
      - Texts
    post:
      summary: Create property value text by language
      description: Saves text for a specific property of the type Text in the specified
        language. The ID of the property and the language must be specified.
      operationId: postRestItemsItemVariationsVariationVariationPropertiesPropertyTexts
      x-api-path-slug: restitemsitemidvariationsvariationidvariation-propertiespropertyidtexts-post
      parameters:
      - in: body
        name: /rest/items/{itemId}/variations/{variationId}/variation_properties/{propertyId}/texts
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: itemId
      - in: path
        name: propertyId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Property
      - Value
      - Text
      - By
      - Language
  /rest/listings/markets/texts:
    get:
      summary: List listing market texts
      description: Lists listing market texts by filter options.
      operationId: getRestListingsMarketsTexts
      x-api-path-slug: restlistingsmarketstexts-get
      parameters:
      - in: query
        name: contains
        description: Filter that restricts the search result to listing market texts
          which title, subtitle or description contain the given value
      - in: query
        name: id
        description: Filter that restricts the search result to listing market texts
          with specific ID
      - in: query
        name: itemsPerPage
        description: The number of items to list per page
      - in: query
        name: language
        description: Filter that restricts the search result to listing market texts
          for a specific language
      - in: query
        name: listingMarketId
        description: Filter that restricts the search result to listing market texts
          with specific listing market IDs
      - in: query
        name: page
        description: The page of results to search for
      responses:
        200:
          description: OK
      tags:
      - List
      - Listing
      - Market
      - Texts
    post:
      summary: Create a listing market text
      description: Creates a listing market text for a given listing market ID. If
        an entry with same data already exists the request will be ignored and the
        old entry will be returned.
      operationId: postRestListingsMarketsTexts
      x-api-path-slug: restlistingsmarketstexts-post
      parameters:
      - in: body
        name: /rest/listings/markets/texts
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: listingMarketId
        description: The listing market ID this text belongs to
      responses:
        200:
          description: OK
      tags:
      - Listing
      - Market
      - Text
  /rest/items/{itemId}/variations/{variationId}/variation_properties/{propertyId}/texts/{lang}:
    delete:
      summary: Delete property value text by language
      description: Deletes the text saved for a specific property of the type Text
        in the specified language. The ID of the property  and the language must be
        specified.
      operationId: deleteRestItemsItemVariationsVariationVariationPropertiesPropertyTextsLang
      x-api-path-slug: restitemsitemidvariationsvariationidvariation-propertiespropertyidtextslang-delete
      parameters:
      - in: path
        name: itemId
      - in: path
        name: lang
      - in: path
        name: propertyId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Property
      - Value
      - Text
      - By
      - Language
    get:
      summary: Get property value text by language
      description: Gets the value text saved for a specific property of the type Text
        in the specified language. The ID of the property  and the language must be
        specified.
      operationId: getRestItemsItemVariationsVariationVariationPropertiesPropertyTextsLang
      x-api-path-slug: restitemsitemidvariationsvariationidvariation-propertiespropertyidtextslang-get
      parameters:
      - in: path
        name: itemId
      - in: path
        name: lang
      - in: path
        name: propertyId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Property
      - Value
      - Text
      - By
      - Language
    put:
      summary: Update property value text by language
      description: Updates the text saved for a specific property of the type Text
        in the specified language. The ID of the property and the language must be
        specified.
      operationId: putRestItemsItemVariationsVariationVariationPropertiesPropertyTextsLang
      x-api-path-slug: restitemsitemidvariationsvariationidvariation-propertiespropertyidtextslang-put
      parameters:
      - in: body
        name: /rest/items/{itemId}/variations/{variationId}/variation_properties/{propertyId}/texts/{lang}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: itemId
      - in: path
        name: lang
      - in: path
        name: propertyId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Property
      - Value
      - Text
      - By
      - Language
  /rest/listings/markets/texts/{id}:
    delete:
      summary: Delete a listing market text
      description: Deletes a listing market text for a given listing market text ID.
      operationId: deleteRestListingsMarketsTexts
      x-api-path-slug: restlistingsmarketstextsid-delete
      parameters:
      - in: path
        name: id
      - in: query
        name: lang
        description: The listing market text language that should be updated
      - in: query
        name: listingMarketId
        description: The listing market ID this text belongs to
      responses:
        200:
          description: OK
      tags:
      - Listing
      - Market
      - Text
    get:
      summary: Get a listing market text
      description: Gets a listing market text by providing its ID.
      operationId: getRestListingsMarketsTexts
      x-api-path-slug: restlistingsmarketstextsid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Listing
      - Market
      - Text
  /rest/listings/markets/texts/{listingMarketId}/{lang}:
    put:
      summary: Update a listing market text
      description: Updates a listing market text for a given listing market ID and
        language.
      operationId: putRestListingsMarketsTextsListingmarketLang
      x-api-path-slug: restlistingsmarketstextslistingmarketidlang-put
      parameters:
      - in: body
        name: /rest/listings/markets/texts/{listingMarketId}/{lang}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: lang
      - in: path
        name: listingMarketId
      responses:
        200:
          description: OK
      tags:
      - Listing
      - Market
      - Text
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