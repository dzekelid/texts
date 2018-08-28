---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Add a Text Widget
  description: Add a new Text Widget to the specified playlist
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /playlist/widget/text/{playlistId}:
    post:
      summary: Add a Text Widget
      description: Add a new Text Widget to the specified playlist
      operationId: WidgetTextAdd
      x-api-path-slug: playlistwidgettextplaylistid-post
      parameters:
      - in: formData
        name: backgroundcolor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft'
      - in: formData
        name: javaScript
        description: Optional JavaScript
      - in: formData
        name: marqueeInlineSelector
        description: The selector to use for stacking marquee items in a line when
          scrolling left/right
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal) or the Marquee speed in a low to high scale (normal = 1)
      - in: formData
        name: text
        description: Enter the text to display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Text
      - Widget
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