# Open Api Specification 

## `Servers` 

In the `servers` object you specify the basepath of your target server.

- You can also incorporate variables into the server URL that can be populated at runtime by your server. 
- If different paths (endpoints) require different server URLs, you can add the servers object as a property in the path object’s operation object. The locally declared servers URL will override the global servers URL.


```javascript
servers:
  - url: 'https://example.com'
    description: Production server
  - url: 'https://beta.example.com'
    description: Beta server
  - url: 'https://{subdomain}.example.com/{basepath}/{version}'
    description: Some other server
    variables:
        subdomain:
            default: production
            description: description
        version:
            enum:
                - 'v1'
                - 'v2'
            default: 'v1'
        basePath:
            default: api
```