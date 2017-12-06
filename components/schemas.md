# Open Api Specification 

## Schemas Object


The schema refers to the data structure ( the fields, values, and hierarchy of the various objects and properties of a JSON or YAML object.




```YAML

openapi:
info:
servers:
paths:

components:
  schemas:
    NameOfObject:
        type: object
        required:
        - "property1"
        - "property2"
        properties:
            property1:
                type: "string"
                format: 
                description:
                example:
            property2:
                type: "array"
                items: 
                    type:
            property3:
                type: "int32"
                format:
                description:
                example:
security:
tags:
externalDocs:
```

### Example

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