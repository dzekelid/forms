---
swagger: "2.0"
x-collection-name: 123FormBuilder
x-complete: 1
info:
  title: ""
  version: 1.0.0
host: api.123contactform.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /forms:
    get:
      summary: List forms
      description: The forms endpoint returns information about the forms. The response
        includes submissions and other details about each form.
      operationId: the-forms-endpoint-returns-information-about-the-forms-the-response-includes-submissions-and-other-d
      x-api-path-slug: forms-get
      parameters:
      - in: query
        name: JWT
        description: JWT authentication token
      - in: query
        name: page
        description: Page number
      - in: query
        name: per_page
        description: The number of forms to get per page in a request
      - in: query
        name: search
        description: Filter form name
      responses:
        200:
          description: OK
      tags:
      - List
      - Forms
  /forms/bulk:
    delete:
      summary: Delete multiple forms
      description: Delete multiple forms
      operationId: delete-multiple-forms
      x-api-path-slug: formsbulk-delete
      parameters:
      - in: formData
        name: form_ids
        description: The IDs of the forms separated by comma
      - in: formData
        name: JWT
        description: JWT authentication token
      responses:
        200:
          description: OK
      tags:
      - Multiple
      - Forms
  /groups/{group_id}/forms:
    get:
      summary: Get all forms in a group
      description: Displays a list of all of the forms within a specific group.
      operationId: displays-a-list-of-all-of-the-forms-within-a-specific-group
      x-api-path-slug: groupsgroup-idforms-get
      parameters:
      - in: path
        name: group_id
        description: The ID of the group
      - in: query
        name: JWT
        description: JWT authentication token
      responses:
        200:
          description: OK
      tags:
      - Forms
      - In
      - Group
---