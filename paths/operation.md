# Open Api Specification 



##### _Table of Contents_
 - [Api Templates](https://samuelmensah.github.io/apitemplates/)
    - [root](https://samuelmensah.github.io/apitemplates/root)
    - [info](https://samuelmensah.github.io/apitemplates/info)
    - [servers](https://samuelmensah.github.io/apitemplates/servers)
    - [tags](https://samuelmensah.github.io/apitemplates/tags)
    - [paths](https://samuelmensah.github.io/apitemplates/paths/path)
      - [operation](https://samuelmensah.github.io/apitemplates/paths/operation)
    - [components](https://samuelmensah.github.io/apitemplates/components/components)
    - [security](https://samuelmensah.github.io/apitemplates/security)
    - [externalDocs](https://samuelmensah.github.io/apitemplates/externaldocs)
    
## Operation Item

Operations are the GET, POST,PUT and Delete methods

  
#### Path Item Fields
- `tags`: optional string summary
- `summary`: optional string summary
- `description`: optional string description
- `externalDocs`: links to documentation for more information about path [`externalDocs`](https://samuelmensah.github.io/apitemplates/components/externaldocs)
- `operationId` : a unique identifier for path
- `parameters` : parameters accepted by the path. Does not include request body parameter[`parameters`](https://samuelmensah.github.io/apitemplates/components/parameters)
- `requestBody` : the request body parameter details for this path [`requestBody`](https://samuelmensah.github.io/apitemplates/components/requestBody)
- `responses` : responses provided from requests with this path [`responses`](https://samuelmensah.github.io/apitemplates/components/responses)
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
