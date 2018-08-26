---
swagger: "2.0"
x-collection-name: GIG & CROWD
x-complete: 1
info:
  title: GIG & Crowd
  version: 1.0.0
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
---