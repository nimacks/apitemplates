# Open Api Specification 

## Servers Object

In the servers object you specify the basepath of your target server.

- You can also incorporate variables into the server URL that can be populated at runtime by your server. 
- If different paths (endpoints) require different server URLs, you can add the servers object as a property in the path object’s operation object. The locally declared servers URL will override the global servers URL.


```YAML
openapi: "3.0.0"

info:

servers:
  - url: https://example.com
    description: Production server
  - url: https://beta.example.com
    description: Beta server
  - url: https://some-other.example.com
    description: Some other server
    variables:
        username:
            default: demo
            description: description
        port:
            enum:
                - '8443'
                - '443'
            default: '8443'
        basePath:
            default: v2

paths:

components:

security:

tags:

externalDocs:
``