# Open Api Specification 

## Operation Item

Operations are the GET, POST,PUT and Delete methods

  
#### Path Item Fields
- `tags`: optional string summary
- `summary`: optional string summary
- `description`: optional string description
- `externalDocs`: links to documentation for more information about path [`externalDocs object`](#)
- `operationId` : a unique identifier for path
- `parameters` : parameters accepted by the path. Does not include request body parameters [`parameters object`](#)
- `requestBody` : the request body parameter details for this path [`requestBody object`](#)
- `responses` : responses provided from requests with this path [`responses object`](#)
- `callbacks` : callbacks are operations performed after a function finishes executing
- `deprecated` : whether the path is deprecated
- `security` : security authorization method used with the operation
- `servers` : a servers object that might differ for this path than the global servers object



### Paths at the root Level
```javascript
paths:
  /aqi:
    get:
      tags:
      - Air Quality
      summary: getAqi
      description: Gets the air quality index
      operationId: GetAqi
      externalDocs:
        description: More details
        url: "https://market.mashape.com/fyhao/weather-13#aqi"
      parameters:

      - name: lat
        in: query
        description: "Latitude coordinates."
        required: true
        style: form
        explode: false
        schema:
          type: string
        example: "37.3708698"

      - name: lng
        in: query
        description: "Longitude coordinates."
        required: true
        style: form
        explode: false
        schema:
          type: string
        example: "-122.037593"

      responses:
        200:
          description: AQI response
          content:
            text/plain:
              schema:
                type: string
                description: AQI response
                example: 52
        400:
          $ref: '#/components/responses/404'


```
