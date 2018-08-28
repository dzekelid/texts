swagger: "2.0"
x-collection-name: CallFire
x-complete: 1
info:
  title: CallFire
  description: callfire
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
    get:
      summary: Find a specific auto reply
      description: Returns a single TextAutoReply instance for a given text auto reply
        id
      operationId: getTextAutoReply
      x-api-path-slug: textsautoreplysid-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a text auto reply
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Auto-replys
  /texts/broadcasts:
    get:
      summary: Find text broadcasts
      description: Searches for all text broadcasts created by user. Can query on
        label, name, and the current running status of the campaign. Returns a paged
        list of text broadcasts
      operationId: findTextBroadcasts
      x-api-path-slug: textsbroadcasts-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: label
        description: A label of a text broadcast
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: name
        description: A name of text broadcast
      - in: query
        name: offset
        description: Offset to the start of a given page
      - in: query
        name: running
        description: Returns broadcasts only in running state
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
    post:
      summary: Create a text broadcast
      description: Creates a text broadcast campaign using the Text Broadcast API.
        Send a TextBroadcast object in the message body to detail a text broadcast
        campaign. A campaign can be created without contacts and with bare minimum
        configuration, but contacts have to be added further on to use the campaign.
        It supports scheduling, retry logic, pattern-based messages.
      operationId: createTextBroadcast
      x-api-path-slug: textsbroadcasts-post
      parameters:
      - in: body
        name: body
        description: A TextBroadcast object
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: start
        description: If true then starts the campaign immediately (not required)
      - in: query
        name: strictValidation
        description: Turns on strict validation for recipients
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
  /texts/broadcasts/{id}:
    get:
      summary: Find a specific text broadcast
      description: Returns a single TextBroadcast instance for a given text broadcast
        id
      operationId: getTextBroadcast
      x-api-path-slug: textsbroadcastsid-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a text broadcast
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
    put:
      summary: Update a text broadcast
      description: Allows modifying the configuration of existing text broadcast campaign.
        See TextBroadcast for more information on what can/can't be updated on this
        API
      operationId: updateTextBroadcast
      x-api-path-slug: textsbroadcastsid-put
      parameters:
      - in: body
        name: body
        description: A TextBroadcast object
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: An id of a text broadcast
      - in: query
        name: strictValidation
        description: Turns on strict validation for recipients
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
  /texts/broadcasts/{id}/archive:
    post:
      summary: Archive text broadcast
      description: Archives a text broadcast (and hides it in the search results)
      operationId: archiveTextBroadcast
      x-api-path-slug: textsbroadcastsidarchive-post
      parameters:
      - in: path
        name: id
        description: An id of a text broadcast to archive
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Archive
  /texts/broadcasts/{id}/batches:
    get:
      summary: Find batches in a text broadcast
      description: This endpoint will enable the user to page through all of the batches
        for a particular text broadcast campaign
      operationId: getTextBroadcastBatches
      x-api-path-slug: textsbroadcastsidbatches-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a text broadcast
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: offset
        description: Offset to the start of a given page
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Batches
    post:
      summary: Add batches to a text broadcast
      description: Allows adding an extra batches to an already created text broadcast
        campaign. The batches which being  added pass the CallFire validation process
        (unlike in the recipients version of this API). That is why using of a scrubDuplicates
        flag remove duplicates from your batch. Batches may be added as a contact
        list id, a list of contact ids, or a list of numbers
      operationId: addTextBroadcastBatch
      x-api-path-slug: textsbroadcastsidbatches-post
      parameters:
      - in: body
        name: body
        description: A request object
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: An id of a text broadcast
      - in: query
        name: strictValidation
        description: Turns on strict validation for recipients
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Batches
  /texts/broadcasts/{id}/recipients:
    post:
      summary: Add recipients to a text broadcast
      description: Use this API to add recipients to a text broadcast which is already
        created. Post a list of Recipient objects to be immediately added to the text
        broadcast campaign. These contacts will not go through validation process,
        and will be acted upon as they are added. Recipients may be added as a list
        of contact ids, or list of numbers
      operationId: addTextBroadcastRecipients
      x-api-path-slug: textsbroadcastsidrecipients-post
      parameters:
      - in: body
        name: body
        description: A list of the TextRecipient objects
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a text broadcast
      - in: query
        name: strictValidation
        description: Turns on strict validation for recipients
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Recipients
  /texts/broadcasts/{id}/start:
    post:
      summary: Start text broadcast
      description: Starts a text broadcast
      operationId: startTextBroadcast
      x-api-path-slug: textsbroadcastsidstart-post
      parameters:
      - in: path
        name: id
        description: An id of a text broadcast to start
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Start
  /texts/broadcasts/{id}/stats:
    get:
      summary: Get statistics on text broadcast
      description: 'Returns the broadcast statistics. Example: total number of the
        sent/received actions, total cost, number of remaining outbound actions, error
        count, etc'
      operationId: getTextBroadcastStats
      x-api-path-slug: textsbroadcastsidstats-get
      parameters:
      - in: query
        name: begin
        description: Start of a search find time interval, formatted in unix time
          milliseconds
      - in: query
        name: end
        description: End of a search time interval, formatted in unix time milliseconds
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a text broadcast
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Stats
  /texts/broadcasts/{id}/stop:
    post:
      summary: Stop text broadcast
      description: Stops a text broadcast
      operationId: stopTextBroadcast
      x-api-path-slug: textsbroadcastsidstop-post
      parameters:
      - in: path
        name: id
        description: An Id of a text broadcast
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Stop
  /texts/broadcasts/{id}/texts:
    get:
      summary: Find texts in a text broadcast
      description: This endpoint will enable the user to page through all of the texts
        for a particular text broadcast campaign
      operationId: getTextBroadcastTexts
      x-api-path-slug: textsbroadcastsidtexts-get
      parameters:
      - in: query
        name: batchId
        description: "~"
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a text broadcast
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: offset
        description: Offset to the start of a given page
      responses:
        200:
          description: OK
      tags:
      - Texts
      - Broadcasts
      - Texts
  /texts/{id}:
    get:
      summary: Find a specific text
      description: Returns a single Text instance for a given text id
      operationId: getText
      x-api-path-slug: textsid-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a text
      responses:
        200:
          description: OK
      tags:
      - Texts