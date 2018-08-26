---
swagger: "2.0"
x-collection-name: Trello
x-complete: 1
info:
  title: Trello
  description: this-document-describes-the-rest-api-of-trello-as-published-by-trello-com---a-hrefhttpstrello-comdocsindex-html-target-blankofficial-documentationa--a-hrefhttpstrello-comdocsapi-target-blankthe-html-pages-that-were-scraped-in-order-to-generate-this-specification-a
  termsOfService: https://trello.com/legal
  contact:
    name: Trello
    url: https://trello.com/home
  version: "1.0"
host: trello.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /members/{idMember}/avatar:
    post:
      summary: Post Members Avatar
      description: Post members avatar.
      operationId: addMembersAvatarByIdMember
      x-api-path-slug: membersidmemberavatar-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Avatar to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Avatar
---