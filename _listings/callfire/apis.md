---
name: CallFire
x-slug: callfire
description: Grow your business with virtual phone numbers, IVR, voice broadcasting,
  mass text messaging services and power dialing. Try CallFire for FREE!
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
x-kinRank: "9"
x-alexaRank: "129466"
tags: Texts
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/apis.md
specificationVersion: "0.14"
apis:
- name: Callfire Find texts
  x-api-slug: callfire
  description: Searches for texts sent or received by user. Use "campaignId=0" parameter
    to query for all texts sent through the POST /texts API. See [call states and
    results](https://developers.callfire.com/results-responses-errors.html)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts
  tags: Texts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/texts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/texts-get-openapi.md
- name: Callfire Send texts
  x-api-slug: callfire
  description: Use the /texts API to send individual texts quickly. By default all
    texts are going out from CallFire's dedicated short code 67076
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts
  tags: Texts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/texts-post-openapi.md
- name: Callfire Find auto replies
  x-api-slug: callfire
  description: Find all text autoreplies created by user. Returns a paged list of
    TextAutoReply
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/auto-replys
  tags: Texts,Auto-replys
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsautoreplys-get-openapi.md
- name: Callfire Create an auto reply
  x-api-slug: callfire
  description: CallFire gives you possibility to set up auto reply messages for your
    numbers and keywords. You can set a general auto reply for anyone who texts your
    number, keyword, and/or include a text to match, so that the auto reply would
    be sent only to those who text the matched text
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/auto-replys
  tags: Texts,Auto-replys
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsautoreplys-post-openapi.md
- name: Callfire Delete an auto reply
  x-api-slug: callfire
  description: Deletes a text auto reply and removes the configuration. Can not delete
    a TextAutoReply which is currently active for a campaign
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/auto-replys/{id}
  tags: Texts,Auto-replys
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsautoreplysid-delete-openapi.md
- name: Callfire Find a specific auto reply
  x-api-slug: callfire
  description: Returns a single TextAutoReply instance for a given text auto reply
    id
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/auto-replys/{id}
  tags: Texts,Auto-replys
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsautoreplysid-get-openapi.md
- name: Callfire Find text broadcasts
  x-api-slug: callfire
  description: Searches for all text broadcasts created by user. Can query on label,
    name, and the current running status of the campaign. Returns a paged list of
    text broadcasts
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts
  tags: Texts,Broadcasts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcasts-get-openapi.md
- name: Callfire Create a text broadcast
  x-api-slug: callfire
  description: Creates a text broadcast campaign using the Text Broadcast API. Send
    a TextBroadcast object in the message body to detail a text broadcast campaign.
    A campaign can be created without contacts and with bare minimum configuration,
    but contacts have to be added further on to use the campaign. It supports scheduling,
    retry logic, pattern-based messages.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts
  tags: Texts,Broadcasts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcasts-post-openapi.md
- name: Callfire Find a specific text broadcast
  x-api-slug: callfire
  description: Returns a single TextBroadcast instance for a given text broadcast
    id
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}
  tags: Texts,Broadcasts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsid-get-openapi.md
- name: Callfire Update a text broadcast
  x-api-slug: callfire
  description: Allows modifying the configuration of existing text broadcast campaign.
    See TextBroadcast for more information on what can/can't be updated on this API
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}
  tags: Texts,Broadcasts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsid-put-openapi.md
- name: Callfire Archive text broadcast
  x-api-slug: callfire
  description: Archives a text broadcast (and hides it in the search results)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/archive
  tags: Texts,Broadcasts,Archive
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidarchive-post-openapi.md
- name: Callfire Find batches in a text broadcast
  x-api-slug: callfire
  description: This endpoint will enable the user to page through all of the batches
    for a particular text broadcast campaign
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/batches
  tags: Texts,Broadcasts,Batches
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidbatches-get-openapi.md
- name: Callfire Add batches to a text broadcast
  x-api-slug: callfire
  description: Allows adding an extra batches to an already created text broadcast
    campaign. The batches which being  added pass the CallFire validation process
    (unlike in the recipients version of this API). That is why using of a scrubDuplicates
    flag remove duplicates from your batch. Batches may be added as a contact list
    id, a list of contact ids, or a list of numbers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/batches
  tags: Texts,Broadcasts,Batches
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidbatches-post-openapi.md
- name: Callfire Add recipients to a text broadcast
  x-api-slug: callfire
  description: Use this API to add recipients to a text broadcast which is already
    created. Post a list of Recipient objects to be immediately added to the text
    broadcast campaign. These contacts will not go through validation process, and
    will be acted upon as they are added. Recipients may be added as a list of contact
    ids, or list of numbers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/recipients
  tags: Texts,Broadcasts,Recipients
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidrecipients-post-openapi.md
- name: Callfire Start text broadcast
  x-api-slug: callfire
  description: Starts a text broadcast
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/start
  tags: Texts,Broadcasts,Start
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidstart-post-openapi.md
- name: Callfire Get statistics on text broadcast
  x-api-slug: callfire
  description: 'Returns the broadcast statistics. Example: total number of the sent/received
    actions, total cost, number of remaining outbound actions, error count, etc'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/stats
  tags: Texts,Broadcasts,Stats
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidstats-get-openapi.md
- name: Callfire Stop text broadcast
  x-api-slug: callfire
  description: Stops a text broadcast
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/stop
  tags: Texts,Broadcasts,Stop
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidstop-post-openapi.md
- name: Callfire Find texts in a text broadcast
  x-api-slug: callfire
  description: This endpoint will enable the user to page through all of the texts
    for a particular text broadcast campaign
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/broadcasts/{id}/texts
  tags: Texts,Broadcasts,Texts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsbroadcastsidtexts-get-openapi.md
- name: Callfire Find a specific text
  x-api-slug: callfire
  description: Returns a single Text instance for a given text id
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2//texts/{id}
  tags: Texts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/textsid-get-openapi.md
- name: Callfire
  x-api-slug: callfire
  description: Grow your business with virtual phone numbers, IVR, voice broadcasting,
    mass text messaging services and power dialing. Try CallFire for FREE!
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11768-callfire.jpg
  humanURL: http://www.callfire.com
  baseURL: https://www.callfire.com//v2
  tags: Texts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/texts/master/_listings/callfire/openapi.md
x-common:
- type: x--net-sdk
  url: https://github.com/CallFire/CallFire-CSharp-SDK
- type: x-account-billing
  url: https://answers.callfire.com/hc/en-us/sections/200166268-Billing
- type: x-account-settings
  url: https://answers.callfire.com/hc/en-us/sections/200187056-Account-Settings
- type: x-authentication
  url: https://www.callfire.com/api-documentation/how-do-i-enable-api-on-my-account
- type: x-blog
  url: https://www.callfire.com/blog
- type: x-blog-rss
  url: https://www.callfire.com/blog/feed
- type: x-twitter
  url: https://twitter.com/CallFire
- type: x-case-studies
  url: https://www.callfire.com/case-studies
- type: x-compliance
  url: https://www.callfire.com/legal/compliance
- type: x-contact-form
  url: https://www.callfire.com/contact
- type: x-crunchbase
  url: https://www.crunchbase.com/organization/callfire
- type: x-crunchbase
  url: https://crunchbase.com/organization/callfire
- type: x-developer
  url: https://www.callfire.com/api-documentation
- type: x-documentation
  url: https://www.callfire.com/api-documentation/rest/version/1.1
- type: x-drupal-plugin
  url: https://github.com/CallFire/CallFire-Drupal-Integration
- type: x-email
  url: answers@callfire.com
- type: x-email
  url: support@callfire.com
- type: x-facebook
  url: https://www.facebook.com/callfire
- type: x-faq
  url: https://answers.callfire.com/hc/en-us/sections/200193833-FAQs
- type: x-getting-started
  url: https://www.callfire.com/help/docs/getting-started
- type: x-github
  url: https://github.com/callfire
- type: x-glossary
  url: https://www.callfire.com/help/glossary/communications
- type: x-google-plus
  url: https://plus.google.com/100142045997033051154
- type: x-messages
  url: https://www.callfire.com/ui/number/messages?6
- type: x-partners
  url: https://www.callfire.com/partners
- type: x-phone
  url: 1.877.897.3473
- type: x-php-sdk
  url: https://github.com/CallFire/CallFire-PHP-SDK
- type: x-pricing
  url: https://www.callfire.com/pricing
- type: x-privacy
  url: https://www.callfire.com/legal/privacy
- type: x-selfservice-registration
  url: https://www.callfire.com/ui/register?1
- type: x-terms-of-service
  url: https://www.callfire.com/legal/terms
- type: x-tickets
  url: https://answers.callfire.com/hc/en-us/requests/new
- type: x-tour
  url: javascript:;
- type: x-videos
  url: https://answers.callfire.com/hc/en-us/articles/200849247-Videos
- type: x-webinars
  url: https://answers.callfire.com/hc/en-us/articles/202174798-Webinars
- type: x-website
  url: http://www.callfire.com
- type: x-wordpress-plugin
  url: https://github.com/CallFire/CallFire-WordPress-Integration
- type: x-youtube
  url: https://www.youtube.com/user/CallFireTelephony
- type: x-zapier
  url: https://zapier.com/zapbook/callfire/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---