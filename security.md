# Open Api Specification 

##### _Table of Contents_
 - [Api Templates](https://samuelmensah.github.io/apitemplates/)
    - [root](https://samuelmensah.github.io/apitemplates/root)
    - [info](https://samuelmensah.github.io/apitemplates/info)
    - [servers](https://samuelmensah.github.io/apitemplates/servers)
    - [tags](https://samuelmensah.github.io/apitemplates/tags)
    - [paths](https://samuelmensah.github.io/apitemplates/paths/path)
    - [components](https://samuelmensah.github.io/apitemplates/components/components)
    - [security](https://samuelmensah.github.io/apitemplates/security)
    - [externalDocs](https://samuelmensah.github.io/apitemplates/externaldocs)
    
## Security 

### `Scheme`
Swagger UI supports four authorization schemes:

- API key
- HTTP
- OAuth 2.0
- Open ID Connect

```Yaml
    tags (array)
        name(string):
        description(string):
```

At the root level of your OpenAPI document, add a security object that defines the global method we’re using for security:
### Security at the root Level
```javascript
security:
- Api-Key: []
```

### Security at the path Level

All paths will use the Api-Key security method by default unless it’s overridden by a value at the path object level. For example, at the path level we could overwrite the global security method as follows:

```javascript
paths:

/weatherdata:
  get:
    ...
    security:
    - Some-Other-Key: []
```