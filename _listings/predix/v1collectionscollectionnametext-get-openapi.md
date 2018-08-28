---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Intelligent Mapping Free text search of a feature collection
  description: |-
    Returns GeoJSON of type FeatureCollection containing all GeoJSON features from the named collection that match
    the supplied search string.

    The search text consists of one or more strings that can be space or comma separated. A match with a given
    feature occurs only if an exact match can be found for each of the strings in the search text amongst a
    concatenation of the values of child members of the top level 'properties' member of the feature,
    together with the value of its GeoJSON id. The matching is case insensitve, partial matches and
    wildcard searching is not supported.

    Examples of search text:

     - 28,West End,Histon
     - 240.000 V
     - Company Owned
  version: 1.0.0
host: insights-api.data-services.predix.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/collections/{collectionName}/text:
    get:
      summary: Free text search of a feature collection
      description: |-
        Returns GeoJSON of type FeatureCollection containing all GeoJSON features from the named collection that match
        the supplied search string.

        The search text consists of one or more strings that can be space or comma separated. A match with a given
        feature occurs only if an exact match can be found for each of the strings in the search text amongst a
        concatenation of the values of child members of the top level 'properties' member of the feature,
        together with the value of its GeoJSON id. The matching is case insensitve, partial matches and
        wildcard searching is not supported.

        Examples of search text:

         - 28,West End,Histon
         - 240.000 V
         - Company Owned
      operationId: returns-geojson-of-type-featurecollection-containing-all-geojson-features-from-the-named-collection-
      x-api-path-slug: v1collectionscollectionnametext-get
      parameters:
      - in: query
        name: No Name
      - in: query
        name: q
        description: The search text
      responses:
        200:
          description: OK
      tags:
      - Free
      - Text
      - Search
      - Of
      - Feature
      - Collection
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