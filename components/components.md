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

## Components

Holds a set of reusable objects for different aspects of the OAS. All objects defined within the components object will have no effect on the API unless they are explicitly referenced from properties outside the components object.


```Yaml
    responses
        'Name'
            description (string)
            headers (object)
            content (object)
            links (object)
```


```javascript

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