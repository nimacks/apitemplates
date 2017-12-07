# Open Api Specification 

## Parameter 

Describes a single operation parameter.

A unique parameter is defined by a combination of a name and location.

#### Fields

- name* : name of the parameter
- in* : the location of the parameter [query,header,path,cookie]
- description: a brief description of the parameter
- required*: determines whether this parameter is mandatory
- deprecated: specifies that a parameter is deprecated
- allowEmptyValue: sets the ability to pass empty-valued paramters  


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
