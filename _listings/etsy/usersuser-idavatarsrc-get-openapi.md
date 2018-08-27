---
swagger: "2.0"
x-collection-name: Etsy
x-complete: 0
info:
  title: Etsy Get Users User Avatar Src
  description: Get avatar image source
  version: 1.0.0
host: openapi.etsy.com
basePath: /v2/private/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{user_id}/avatar:
    post:
      summary: Post Users User Avatar
      description: Upload a new user avatar image
      operationId: postUsersUserAvatar
      x-api-path-slug: usersuser-idavatar-post
      parameters:
      - in: query
        name: image
      - in: query
        name: src
      - in: path
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Avatar
  /users/{user_id}/avatar/src:
    get:
      summary: Get Users User Avatar Src
      description: Get avatar image source
      operationId: getUsersUserAvatarSrc
      x-api-path-slug: usersuser-idavatarsrc-get
      parameters:
      - in: path
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Avatar
      - Src
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