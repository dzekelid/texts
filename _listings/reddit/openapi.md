swagger: "2.0"
x-collection-name: Reddit
x-complete: 1
info:
  title: Reddit
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