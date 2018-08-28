---
swagger: "2.0"
x-collection-name: 123FormBuilder
x-complete: 0
info:
  title: 123FormBuilder Create a new form
  version: 1.0.0
  description: Create a new form
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
    post:
      summary: Create a new form
      description: Create a new form
      operationId: create-a-new-form
      x-api-path-slug: forms-post
      parameters:
      - in: formData
        name: active
        description: Form activity status
      - in: formData
        name: active_date_from
        description: If activity status is 1, this field is required
      - in: formData
        name: active_date_to
        description: If activity status is 1, this field is required
      - in: formData
        name: active_days
        description: If activity status is 4, this field is required
      - in: formData
        name: group_id
        description: The ID of the group in which you want to create the form
      - in: formData
        name: JWT
        description: JWT authentication token
      - in: formData
        name: name
        description: The name of the new form
      responses:
        200:
          description: OK
      tags:
      - New
      - Form
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