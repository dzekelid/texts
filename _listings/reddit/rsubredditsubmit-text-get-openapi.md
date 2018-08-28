---
swagger: "2.0"
x-collection-name: Reddit
x-complete: 0
info:
  title: Reddit Get Subreddit Submit Text
  description: Get the submission text for the subreddit.
  version: 1.0.0
host: www.reddit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  '{/r/subreddit}/submit_text':
    get:
      summary: Get Subreddit Submit Text
      description: Get the submission text for the subreddit.
      operationId: get&nbsp;RSubredditSubmitText
      x-api-path-slug: rsubredditsubmit-text-get
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Submit
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