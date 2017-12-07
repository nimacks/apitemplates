# Open Api Specification 

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