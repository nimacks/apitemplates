# Open Api Specification 

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
### Tags at the root Level
```javascript
security:
- Api-Key: []
```

### Tags at the path Level

All paths will use the Api-Key security method by default unless it’s overridden by a value at the path object level. For example, at the path level we could overwrite the global security method as follows:

```javascript
paths:

/weatherdata:
  get:
    ...
    security:
    - Some-Other-Key: []
```