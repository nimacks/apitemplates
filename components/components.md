# Open Api Specification 

## Components

Holds a set of reusable objects for different aspects of the OAS. All objects defined within the components object will have no effect on the API unless they are explicitly referenced from properties outside the components object.

<!-- TOC -->

- [Open Api Specification](#open-api-specification)
    - [Components](#components)

<!-- /TOC -->

```Yaml
    responses
        'Name'
            description (string)
            headers (object)
            content (object)
            links (object)
```


```YAML

openapi:
info:
servers:
paths:

components:
  schemas:
  responses:
  parameters:
  examples:
  requestBody:
  headers:
  securitySchemes:
  links:
  callbacks:

security:
tags:
externalDocs:
```