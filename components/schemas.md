# Open Api Specification 

## Schemas Object


The schema refers to the data structure ( the fields, values, and hierarchy of the various objects and properties of a JSON or YAML object.


```YAML
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