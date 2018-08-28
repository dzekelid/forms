---
swagger: "2.0"
x-collection-name: EhrScape
x-complete: 0
info:
  title: Ehr Scape Electronic Health Record APIs Loads a Think!Ehr form.
  description: Loads a think!ehr form..
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: rest.ehrscape.com
basePath: /rest/v1
paths:
  /form:
    get:
      summary: Lists Think!Ehr forms.
      description: Lists think!ehr forms..
      operationId: getForms
      x-api-path-slug: form-get
      responses:
        200:
          description: OK
      tags:
      - Form
  /form/{name}/{version}:
    get:
      summary: Loads a Think!Ehr form.
      description: Loads a think!ehr form..
      operationId: getForm
      x-api-path-slug: formnameversion-get
      parameters:
      - in: path
        name: name
        description: The name of the form
      - in: query
        name: resources
        description: Which, if any, resources to expand
      - in: path
        name: version
        description: The version of the form, such as 1
      responses:
        200:
          description: OK
      tags:
      - Form
      - Name
      - Version
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