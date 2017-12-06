# Open Api Specification 

## Response Object
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
    '200':
        description: a pet to be returned
        content: 
            application/json:
            schema:
                $ref: '#/components/schemas/Pet'
        headers:
        X-Rate-Limit-Limit:
            description: The number of allowed requests in the current period
            type: integer
        X-Rate-Limit-Remaining:
            description: The number of remaining requests in the current period
            type: integer
        X-Rate-Limit-Reset:
            description: The number of seconds left in the current period
            type: integer
    default:
        description: Unexpected error
        content:
            application/json:
            schema:
                $ref: '#/components/schemas/ErrorModel'
    description: A simple string response
    content:
        text/plain:
        schema:
            type: string
        example: 'whoa!'


```

Headers Object
Lists the headers that can be sent in a response or forwarded via a link. Note that RFC 7230 states header names are case insensitive.
```YAML
    headers:
        X-Rate-Limit-Limit:
    description: The number of allowed requests in the current period
    schema:
        type: integer
```






### Example

```YAML

```