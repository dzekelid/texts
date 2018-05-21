---
swagger: "2.0"
x-collection-name: CallFire
x-complete: 0
info:
  title: Callfire Delete an auto reply
  description: Deletes a text auto reply and removes the configuration. Can not delete
    a TextAutoReply which is currently active for a campaign
  termsOfService: https://www.callfire.com/legal/terms
  contact:
    name: CallFire
    url: https://www.callfire.com
    email: support@callfire.com
  version: 1.0.0
host: www.callfire.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /texts:
    get:
      summary: Find texts
      description: Searches for texts sent or received by user. Use "campaignId=0"
        parameter to query for all texts sent through the POST /texts API. See [call
        states and results](https://developers.callfire.com/results-responses-errors.html)
      operationId: findTexts
      x-api-path-slug: texts-get
      parameters:
      - in: query
        name: batchId
        description: An Id of a contact batch, queries for texts which are used in
          the particular contact batch
      - in: query
        name: campaignId
        description: An id of a campaign, queries for texts inside a particular campaign
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: fromNumber
        description: A phone number in E
      - in: query
        name: id
        description: List of Text ids to search for, if ids specified other query
          params ignored
      - in: query
        name: inbound
        description: Specify true for inbound or false for outbounds
      - in: query
        name: intervalBegin
        description: Start of the find time interval, formatted in unix time milliseconds
      - in: query
        name: intervalEnd
        description: End of the find time interval, formatted in unix time milliseconds
      - in: query
        name: label
        description: A label of a text message
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: offset
        description: Offset to the start of a given page
      - in: query
        name: results
        description: 'Expected text results in comma separated string, available values:
          SENT, RECEIVED, DNT, TOO_BIG, INTERNAL_ERROR, CARRIER_ERROR, CARRIER_TEMP_ERROR,
          UNDIALED'
      - in: query
        name: states
        description: 'Expected text statuses in comma separated string, available
          values: READY, SELECTED, CALLBACK, FINISHED, DISABLED, DNC, DUP, INVALID,
          TIMEOUT, PERIOD_LIMIT'
      - in: query
        name: toNumber
        description: A phone number in E
      responses:
        200:
          description: OK
      tags:
      - Texts
    post:
      summary: Send texts
      description: Use the /texts API to send individual texts quickly. By default
        all texts are going out from CallFire's dedicated short code 67076
      operationId: sendTexts
      x-api-path-slug: texts-post
      parameters:
      - in: body
        name: body
        description: List of TextRecipient objects
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: campaignId
        description: Specifies a campaignId to send texts through a previously created
          campaign
      - in: query
        name: defaultMessage
        description: Text message can be overridden by TextRecipient
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: strictValidation
        description: Turns on strict validation for recipients
      responses:
        200:
          description: OK
      tags:
      - Texts
  /texts/auto-replys:
    get:
      summary: Find auto replies
      description: Find all text autoreplies created by user. Returns a paged list
        of TextAutoReply
      operationId: findTextAutoReplys
      x-api-path-slug: textsautoreplys-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: number
        description: Phone number in E
      - in: query
        name: offset
        description: Offset to the start of a given page
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Auto-replys
    post:
      summary: Create an auto reply
      description: CallFire gives you possibility to set up auto reply messages for
        your numbers and keywords. You can set a general auto reply for anyone who
        texts your number, keyword, and/or include a text to match, so that the auto
        reply would be sent only to those who text the matched text
      operationId: createTextAutoReply
      x-api-path-slug: textsautoreplys-post
      parameters:
      - in: body
        name: body
        description: TextAutoReply object, keyword or number should be specified with
          response message and text to match if needed
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Auto-replys
  /texts/auto-replys/{id}:
    delete:
      summary: Delete an auto reply
      description: Deletes a text auto reply and removes the configuration. Can not
        delete a TextAutoReply which is currently active for a campaign
      operationId: deleteTextAutoReply
      x-api-path-slug: textsautoreplysid-delete
      parameters:
      - in: path
        name: id
        description: An id of a text auto reply
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Auto-replys
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