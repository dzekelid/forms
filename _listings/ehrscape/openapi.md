swagger: "2.0"
x-collection-name: EhrScape
x-complete: 1
info:
  title: EhrScape Terminology APIs
  description: validates-and-resolves-terminology-codes
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: rest.ehrscape.com
basePath: /terminology-adapter/rest
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
  /form/{name}/{version}/resource/{resource}:
    get:
      summary: Loads a Think!Ehr form resource content.
      description: Loads a think!ehr form resource content..
      operationId: getFormResource
      x-api-path-slug: formnameversionresourceresource-get
      parameters:
      - in: query
        name: envelope
        description: Whether or not to wrap a response in a JSON object that includes
          meta-data, or just return the resource content (default)
      - in: path
        name: name
        description: The name of the form
      - in: path
        name: resource
        description: The name of the form resource
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
      - Resource
      - Resource