---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Get Floodlight Activity
  version: 1.0.0
  description: Gets one floodlight activity by ID.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /userprofiles/{profileId}/floodlightActivities:
    get:
      summary: Get Floodlight Activities
      description: Retrieves a list of floodlight activities, possibly filtered. This
        method supports paging.
      operationId: dfareporting.floodlightActivities.list
      x-api-path-slug: userprofilesprofileidfloodlightactivities-get
      parameters:
      - in: query
        name: advertiserId
        description: Select only floodlight activities for the specified advertiser
          ID
      - in: query
        name: floodlightActivityGroupIds
        description: Select only floodlight activities with the specified floodlight
          activity group IDs
      - in: query
        name: floodlightActivityGroupName
        description: Select only floodlight activities with the specified floodlight
          activity group name
      - in: query
        name: floodlightActivityGroupTagString
        description: Select only floodlight activities with the specified floodlight
          activity group tag string
      - in: query
        name: floodlightActivityGroupType
        description: Select only floodlight activities with the specified floodlight
          activity group type
      - in: query
        name: floodlightConfigurationId
        description: Select only floodlight activities for the specified floodlight
          configuration ID
      - in: query
        name: ids
        description: Select only floodlight activities with the specified IDs
      - in: query
        name: maxResults
        description: Maximum number of results to return
      - in: query
        name: pageToken
        description: Value of the nextPageToken from the previous result page
      - in: path
        name: profileId
        description: User profile ID associated with this request
      - in: query
        name: searchString
        description: Allows searching for objects by name or ID
      - in: query
        name: sortField
        description: Field by which to sort the list
      - in: query
        name: sortOrder
        description: Order of sorted results, default is ASCENDING
      - in: query
        name: tagString
        description: Select only floodlight activities with the specified tag string
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Floodlight Activity
    patch:
      summary: Update Floodlight Activity
      description: Updates an existing floodlight activity. This method supports patch
        semantics.
      operationId: dfareporting.floodlightActivities.patch
      x-api-path-slug: userprofilesprofileidfloodlightactivities-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: id
        description: Floodlight activity ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Floodlight Activity
    post:
      summary: Insert Floodlight Activity
      description: Inserts a new floodlight activity.
      operationId: dfareporting.floodlightActivities.insert
      x-api-path-slug: userprofilesprofileidfloodlightactivities-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Floodlight Activity
    put:
      summary: Update Floodlight Activity
      description: Updates an existing floodlight activity.
      operationId: dfareporting.floodlightActivities.update
      x-api-path-slug: userprofilesprofileidfloodlightactivities-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Floodlight Activity
  /userprofiles/{profileId}/floodlightActivities/generatetag:
    post:
      summary: Generate Tag for Floodlight Activity
      description: Generates a tag for a floodlight activity.
      operationId: dfareporting.floodlightActivities.generatetag
      x-api-path-slug: userprofilesprofileidfloodlightactivitiesgeneratetag-post
      parameters:
      - in: query
        name: floodlightActivityId
        description: Floodlight activity ID for which we want to generate a tag
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Floodlight Activity
  /userprofiles/{profileId}/floodlightActivities/{id}:
    delete:
      summary: Delete Floodlight Activity
      description: Deletes an existing floodlight activity.
      operationId: dfareporting.floodlightActivities.delete
      x-api-path-slug: userprofilesprofileidfloodlightactivitiesid-delete
      parameters:
      - in: path
        name: id
        description: Floodlight activity ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Floodlight Activity
    get:
      summary: Get Floodlight Activity
      description: Gets one floodlight activity by ID.
      operationId: dfareporting.floodlightActivities.get
      x-api-path-slug: userprofilesprofileidfloodlightactivitiesid-get
      parameters:
      - in: path
        name: id
        description: Floodlight activity ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Floodlight Activity
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