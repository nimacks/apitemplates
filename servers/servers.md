# Open Api Specification 

## Servers Object

In the servers object you specify the basepath of your target server.

- You can also incorporate variables into the server URL that can be populated at runtime by your server. 
- If different paths (endpoints) require different server URLs, you can add the servers object as a property in the path object’s operation object. The locally declared servers URL will override the global servers URL.

```YAML

openapi:
info:

servers:
  - url: 
    description: 
  - url: 
    description: 
  - url: 
    description: 
    variables:
        username:
            default: 
            description: 
        port:
            enum:
                - '[PORT #1]'
                - '[PORT #2]'
            default: 
        basePath:
            default: 

paths:
components:
security:
tags:
externalDocs:
```

> #### Example

```YAML
openapi: "3.0.0"

info:

servers:
  - url: https://simple-weather.p.mashape.com
    description: Production server
  - url: https://beta.simple-weather.p.mashape.com
    description: Beta server
  - url: https://some-other.simple-weather.p.mashape.com
    description: Some other server
    variables:
        username:
      # note! no enum here means it is an open value
            default: demo
            description: this value is assigned by the service provider, in this example `gigantic-server.com`
        port:
            enum:
                - '8443'
                - '443'
            default: '8443'
        basePath:
        # open meaning there is the opportunity to use special base paths as assigned by the provider, default is `v2`
            default: v2

paths:

components:

security:

tags:

externalDocs:
``