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

## Parameters 

Describes a single operation parameter.

A unique parameter is defined by a combination of a name and location.

#### Fields

- `name*` : name of the parameter
- `in*` : the location of the parameter [query,header,path,cookie]
- `description`: a brief description of the parameter
- `required*`: determines whether this parameter is mandatory
- `deprecated`: specifies that a parameter is deprecated
- `allowEmptyValue`: sets the ability to pass empty-valued paramters  
- `style` : how the parameters data is serialized
-  `explode` : advanced parameter related to arrays
-  `allowReserved`: whether reserved characters are allowed
-  `schema` : The schema or model for the parameter
-  `example` : an example of the media type


### Tags at the root Level
```javascript
parameters:
    latParam:
      name: lat
      in: query
      description: "Latitude coordinates."
      required: true
      style: form
      explode: false
      schema:
        type: string
      example: "37.3708698"
    lngParam:
      name: lng
      in: query
      description: "Longitude coordinates."
      required: true
      style: form
      explode: false
      schema:
        type: string
      example: "-122.037593"
```
