---
swagger: "2.0"
x-collection-name: Etsy
x-complete: 1
info:
  title: Etsy
  description: bring-etsys-handmade-marketplace-and-community-into-your-apps-
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
---