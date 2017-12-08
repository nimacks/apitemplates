# OpenApi Templates 


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
    

## ExternalDocs 

The externalDocs object lets you link to external documentation. You can also provide links to external docs in the paths object.

```Yaml
    externalDocs (array)
        name(string):
        description(string):
```

### External Docs at the root Level
```javascript
externalDocs:
  description: Full documentation for the API
  url: https://market.mashape.com/fyhao/weather-13
```

