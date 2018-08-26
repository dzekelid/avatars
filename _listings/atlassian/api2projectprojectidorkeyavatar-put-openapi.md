---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Update project avatar
  description: ""
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
  /api/2/universal_avatar/type/{type}/owner/{entityId}:
    get:
      summary: Get avatars
      description: ""
      operationId: com.atlassian.jira.rest.v2.issue.UniversalAvatarResource.getAvatars_get
      x-api-path-slug: api2universal-avatartypetypeownerentityid-get
      parameters:
      - in: path
        name: entityId
      - in: path
        name: type
      responses:
        200:
          description: OK
      tags:
      - Avatars
  /api/2/issuetype/{id}/avatar2:
    post:
      summary: Create issue type avatar
      description: |-
        Creates an avatar for the issue type. Specify the avatar's local file location as binary data in the body of the request. Also, include the following headers:

        *   `X-Atlassian-Token: no-check`
        *   `Content-Type: image/_image type_` Valid image types are JPEG, GIF, or PNG.

        For example: `curl --request POST \ --user email@example.com: \ --header 'X-Atlassian-Token: no-check' \ --header 'Content-Type: image/< image_type>' \ --data-binary "" \ --url 'https://your-domain.atlassian.net/rest/api/2/issuetype/{issueTypeId}'This` The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image. The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size. After creating the avatar, use [Update issue type](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-put) to set it as the issue type's active avatar. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.createIssueTypeAvatar_post
      x-api-path-slug: api2issuetypeidavatar2-post
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      - in: query
        name: size
        description: The length of each side of the crop region
      - in: query
        name: x
        description: The X coordinate of the top-left corner of the crop region
      - in: query
        name: "y"
        description: The Y coordinate of the top-left corner of the crop region
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Avatar
  /api/2/project/{projectIdOrKey}/avatar:
    put:
      summary: Update project avatar
      description: ""
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.updateProjectAvatar_put
      x-api-path-slug: api2projectprojectidorkeyavatar-put
      parameters:
      - in: path
        name: projectIdOrKey
      responses:
        200:
          description: OK
      tags:
      - Project
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