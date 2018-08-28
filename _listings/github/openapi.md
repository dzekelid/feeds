swagger: "2.0"
x-collection-name: GitHub
x-complete: 1
info:
  title: GitHub
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /feeds:
    get:
      summary: Get Feeds
      description: |-
        List Feeds.
        GitHub provides several timeline resources in Atom format. The Feeds API
         lists all the feeds available to the authenticating user.
      operationId: list-feedsgithub-provides-several-timeline-resources-in-atom-format-the-feeds-api-lists-all-the-feed
      x-api-path-slug: feeds-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      responses:
        200:
          description: OK
      tags:
      - Feeds