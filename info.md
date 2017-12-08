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



### Info Object

The info object contains basic information about your API, including the title, a description, version, link to the license, link to the terms of service, and contact information. Many of the properties are optional.



```javascript
info:
  title: 'API title'
  description: "Api Description"
  version: '1.0'
  termsOfService: 'https://example.com/terms/'
  contact:
    name: John Doe
    url: 'https://example/johndoe'
    email: john@doe.com
  license:
    name: Limited license
    url: 'https://example.com/terms/'

```
