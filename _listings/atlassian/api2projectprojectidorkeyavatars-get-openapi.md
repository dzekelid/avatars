---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get all project avatars
  description: Returns all project avatars visible for the currently logged in user.
    The avatars are grouped into system avatars and custom avatars.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/avatar/{type}/system:
    get:
      summary: Get all system avatars
      description: Returns all system avatars of the given type.
      operationId: com.atlassian.jira.rest.v2.issue.AvatarResource.getAllSystemAvatars_get
      x-api-path-slug: api2avatartypesystem-get
      parameters:
      - in: path
        name: type
        description: the avatar type
      responses:
        200:
          description: OK
      tags:
      - System
      - Avatars
  /api/2/project/{projectIdOrKey}/avatars:
    get:
      summary: Get all project avatars
      description: Returns all project avatars visible for the currently logged in
        user. The avatars are grouped into system avatars and custom avatars.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getAllProjectAvatars_get
      x-api-path-slug: api2projectprojectidorkeyavatars-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Avatars
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