# Open Api Templates

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

## Response 
A container for the expected responses of an operation. The container maps a HTTP response code to the expected response.

Describes a single response from an API Operation, including design-time, static links to operations based on the response.

The Responses Object MUST contain at least one response code, and it SHOULD be the response for a successful operation call.

```Yaml
    responses
        'Name'
            description (string)
            headers (object)
            content (object)
            links (object)
```

```YAML

components:
  responses:
    404:
      description: Not found
      content:
        text/plain:
          schema:
            type: string
            description: Not found
            example: Not found
    default:
        description: Unexpected error
        content:
            application/json:
            schema:
                $ref: '#/components/schemas/ErrorModel'
```
