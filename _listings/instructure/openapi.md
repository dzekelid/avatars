swagger: "2.0"
x-collection-name: Instructure
x-complete: 1
info:
  title: Instructure Canvas Utility APIs
  description: canvas-lms-includes-a-rest-api-for-accessing-and-modifying-data-externally-from-the-main-application-in-your-own-programs-and-scripts--
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{user_id}/avatars:
    get:
      summary: List avatar options
      description: List avatar options.
      operationId: list-avatar-options
      x-api-path-slug: usersuser-idavatars-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - User
      - Id
      - Avatars