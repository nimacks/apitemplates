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


## `Tags` 

The `tags` object provides a way to group the paths (endpoints) in the Swagger UI display.

```Yaml
    tags (array)
        name(string):
        description(string):
```

### `Tags` at the root Level
```javascript
tags:
 - name: facilities
   description: Everything about facilities
 - name: Weather Forecast
    description: A full list of details about the current weather.
```

### Tags at the path Level
```javascript
paths:

  /weatherdata:
    get:
      tags:
        - Weather Forecast
      summary: getWeatherData
      description: Get weather forecast with lots of details
      operationId: GetWeatherData
```