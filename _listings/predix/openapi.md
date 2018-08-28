swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
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