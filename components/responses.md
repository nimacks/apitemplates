# Open Api Specification 

## Response Object


Describes a single response from an API Operation, including design-time, static links to operations based on the response.

```Yaml
    responses
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
  responses:
    description: A simple string response
    content:
        text/plain:
        schema:
            type: string
        example: 'whoa!'
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
    links:
        UserRepositories:
            # returns array of '#/components/schemas/repository'
            operationId: getRepositoriesByOwner
            parameters:
                username: $response.body#/username
        UserRepository:
            # returns '#/components/schemas/repository'
            operationId: getRepository
            parameters:
                username: $response.body#/owner/username
                slug: $response.body#/slug


security:
tags:
externalDocs:
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