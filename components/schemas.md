# OpenApi Templates

- [Api Templates](https://samuelmensah.github.io/apitemplates/)
    - [root](https://samuelmensah.github.io/apitemplates/root)
    - [info](https://samuelmensah.github.io/apitemplates/info)
    - [servers](https://samuelmensah.github.io/apitemplates/servers)
    - [tags](https://samuelmensah.github.io/apitemplates/tags)
    - [paths](https://samuelmensah.github.io/apitemplates/paths/path)
    - [components](https://samuelmensah.github.io/apitemplates/components)
        - [callbacks](https://samuelmensah.github.io/apitemplates/components/callbacks)
        - [examples](https://samuelmensah.github.io/apitemplates/components/examples)
        - [headers](https://samuelmensah.github.io/apitemplates/components/headers)
        - [links](https://samuelmensah.github.io/apitemplates/components/links)
        - [parameters](https://samuelmensah.github.io/apitemplates/components/parameters)
        - [requestBody](https://samuelmensah.github.io/apitemplates/components/requestBody)
        - [responses](https://samuelmensah.github.io/apitemplates/components/responses) 
        - [schemas](https://samuelmensah.github.io/apitemplates/components/schemas) 
        - [securitySchemes](https://samuelmensah.github.io/apitemplates/components/securitySchemes) 
    - [security](https://samuelmensah.github.io/apitemplates/security)
    - [externalDocs](https://samuelmensah.github.io/apitemplates/externaldocs)

## Schemas 


The schema refers to the data structure ( the fields, values, and hierarchy of the various objects and properties of a JSON or YAML object.
#### Fields

- `type` : string
- `description` : string
- `format` : `data type formats`
- `default` : default value 
- `items` : items must be present if type is array
- `properties` : a `Schema` object 
- `additionalProperties` : value can be `boolean` or `Schema` object
- `allOf`
- `anyof`
- `not`



```javascript
components:
  schemas:
    Error:
      type: object
      description: 'A generic response body to be returned from the server when an error is caught'
      required:
        - code
        - message
      properties:
        Id:
          type: integer
        code:
          type: string
        message:
          type: string
    IdResult:
      description: 
        A generic response body to be returned from the server with the id of record as part of a CRUD operation
      type: object
      properties:
        id:
          description: 'UUID'
          type: string
```