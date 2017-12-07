# Open Api Specification 

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
