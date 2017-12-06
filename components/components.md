# Open Api Specification 

## Components

Holds a set of reusable objects for different aspects of the OAS. All objects defined within the components object will have no effect on the API unless they are explicitly referenced from properties outside the components object.

<!-- TOC -->

- [Open Api Specification](#open-api-specification)
    - [Components](#components-object)
      - [schemas](#components-object)
      - [responses](#components-object)
      - [parameters](#components-object)
      - [requestBody](#components-object)
      - [headers](#components-object)
      - [securitySchemes](#components-object)
      - [links](#components-object)
      - [callbacks](#components-object)


<!-- /TOC -->

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