---
swagger: "2.0"
x-collection-name: Tumblr
x-complete: 1
info:
  title: Tumblr
  description: ntshare-photos-mobile-apps-and-social-network-using-tumblrs-apis-n----
  version: 1.0.0
host: api.tumblr.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /blog/{base-hostname}/avatar/{size}:
    get:
      summary: Get Blog Base Hostname Avatar Size
      description: Retrieves a blog's avatar in one of 9 different sizes.
      operationId: blog.base_hostname.avatar.size.get
      x-api-path-slug: blogbasehostnameavatarsize-get
      parameters:
      - in: path
        name: base-hostname
        description: The unique hostname of the blog
      - in: path
        name: size
        description: The size of the avatar (square, one value for both length and
          width)
      responses:
        200:
          description: OK
      tags:
      - Blog
      - Base
      - Hostname
      - Avatar
      - Size
---