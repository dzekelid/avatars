---
swagger: "2.0"
x-collection-name: GIG & CROWD
x-complete: 0
info:
  title: GIGANDCROWD Post Account Avatar
  version: 1.0.0
  description: Post account avatar.
host: gigandcrowd.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/account/avatar:
    post:
      summary: Post Account Avatar
      description: Post account avatar.
      operationId: postApiV1AccountAvatar
      x-api-path-slug: apiv1accountavatar-post
      parameters:
      - in: header
        name: Authorization
      - in: query
        name: file
      responses:
        200:
          description: OK
      tags:
      - Account
      - Avatar
  /api/v1/admin/user/{userId}/avatar:
    post:
      summary: Post Admin User Userid Avatar
      description: Post admin user userid avatar.
      operationId: postApiV1AdminUserUserAvatar
      x-api-path-slug: apiv1adminuseruseridavatar-post
      parameters:
      - in: header
        name: Authorization
      - in: query
        name: file
      responses:
        200:
          description: OK
      tags:
      - Admin
      - User
      - Userid
      - Avatar
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