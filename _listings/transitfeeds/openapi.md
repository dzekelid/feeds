swagger: "2.0"
x-collection-name: TransitFeeds
x-complete: 1
info:
  title: TransitFeeds API
  description: api-to-view-feed-information-and-download-feeds-from-transitfeeds-com
  contact:
    name: TransitFeeds.com
    url: https://transitfeeds.com/issues
    email: support@transitfeeds.com
  version: 1.0.0
host: api.transitfeeds.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /getFeeds:
    get:
      summary: Retrieve a list of feeds.
      description: |-
        Used this API to retrieve a list of feeds in the system. Doing so can be usedful to discover feed IDs that
        can be used in other API calls.
      operationId: getFeeds
      x-api-path-slug: getfeeds-get
      parameters:
      - in: query
        name: descendants
        description: If a location is specified in `location`, this flag can be used
          to control if returned feeds must be assigned directly to the location,
          or if feeds belonging to sub-locations can also be returned
      - in: query
        name: key
        description: Your personal API key, used for authentication
      - in: query
        name: limit
        description: The maximum number of results to return
      - in: query
        name: location
        description: This is the unique ID of a location
      - in: query
        name: page
        description: The page number of results to return
      - in: query
        name: type
        description: The type of feeds to return
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Feeds
  /getFeedVersions:
    get:
      summary: Retrieve a list of versions of specified (or all) feeds.
      description: |-
        This API call allows you to easily see every single feed update in the TranstiFeeds.com system. Since this can be quite
        long, it's also possible to filter this list by a single feed ID.
      operationId: getFeedVersions
      x-api-path-slug: getfeedversions-get
      parameters:
      - in: query
        name: err
        description: To include any errors detected when importing this feed in the
          response, specify a valud of `1`
      - in: query
        name: feed
        description: If you only want to retrieve feed versions for a particular feed,
          include its ID here
      - in: query
        name: key
        description: Your personal API key, used for authentication
      - in: query
        name: limit
        description: The maximum number of results to return
      - in: query
        name: page
        description: The page number of results to return
      - in: query
        name: warn
        description: To include any warnings detected when importing this feed in
          the response, specify a valud of `1`
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Versions
      - Of
      - Specified
      - (or
      - )
      - Feeds