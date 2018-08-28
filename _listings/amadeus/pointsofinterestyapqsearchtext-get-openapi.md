---
swagger: "2.0"
x-collection-name: Amadeus
x-complete: 0
info:
  title: Amadeus Get Points Of Interest Yapq Search Text
  description: "Amadeus has partnered with YapQ to bring you point of interest APIs
    with the goal of offering you unbiased ratings of landmarks and tourist attractions.
    YapQ rates these points according to their interest on social media and provides
    Wikipedia content and Geonames ID in a given city. \nYapQ's service indexes millions
    of points around the world, and provides content in 12 different languages. This
    allows you to ensure you catch the must-see sights in a YapQ supported city.\nEach
    point of interest comes with links to content, grading information, location and
    directions to help make discovering your destination easy and fun.\nThis service
    is still under active development, and the response format may change without
    warning. We'd be interested in your feedback - send us an email."
  contact:
    name: Amadeus Innovation and Research
    url: https://sandbox.amadeus.com
  version: 1.0.0
host: api.sandbox.amadeus.com
basePath: /v1.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /points-of-interest/yapq-search-text:
    get:
      summary: Get Points Of Interest Yapq Search Text
      description: "Amadeus has partnered with YapQ to bring you point of interest
        APIs with the goal of offering you unbiased ratings of landmarks and tourist
        attractions. YapQ rates these points according to their interest on social
        media and provides Wikipedia content and Geonames ID in a given city. \nYapQ's
        service indexes millions of points around the world, and provides content
        in 12 different languages. This allows you to ensure you catch the must-see
        sights in a YapQ supported city.\nEach point of interest comes with links
        to content, grading information, location and directions to help make discovering
        your destination easy and fun.\nThis service is still under active development,
        and the response format may change without warning. We'd be interested in
        your feedback - send us an email."
      operationId: getPointsOfInterestYapqSearchText
      x-api-path-slug: pointsofinterestyapqsearchtext-get
      parameters:
      - in: query
        name: category
        description: Filters the resulting points_of_interest to include only results
          which have a least one category containing the given provided word
      - in: query
        name: city_name
        description: The name of the supported city for which you are searching, in
          the selected language
      - in: query
        name: geonames
        description: Setting this to true includes only points of interest with a
          geonames ID
      - in: query
        name: image_size
        description: The size of the images youd like to see in the response
      - in: query
        name: lang
        description: The preferred language of the content related to each point of
          interest
      - in: query
        name: number_of_images
        description: Number of images to display
      - in: query
        name: number_of_results
        description: The maximum number of points of interest to return in the results
          set
      - in: query
        name: social_media
        description: Enabling this includes images from Instagram in the output results
      - in: query
        name: vibes
        description: Includes content that doesnt correspond to an active physical
          place, but which gives the user some background information, or vibe for
          the place they are visiting
      responses:
        200:
          description: OK
      tags:
      - Points
      - Of
      - Interest
      - Yapq
      - Search
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