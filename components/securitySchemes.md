# OpenApi Templates


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


## SecurityScheme 

Defines a security scheme that can be used by the operations. Supported schemes are HTTP authentication, an API key (either as a header or as a query parameter), OAuth2's common flows (implicit, password, application and access code) as defined in RFC6749, and OpenID Connect Discovery.


Properties you can use in the securitySchemes object include the following:

- `type*`: The type of authorization — apiKey, http, oauth2, or openIdConnect.
- `description`: A description of your security method. In Swagger UI, this - description appears in the Authorization modal (see screenshot below). CommonMark Markdown is allowed.
- `name*`: The name of the header value submitted in the request. Used only for apiKey type security.
- `in*`: Specifies where the security key is applied. Options are query, header or - cookie. Used only for apiKey type security.
- `scheme`. Used with http type authorization.
- `bearerFormat`. Used with http type authorization.
- `flows` (object): Used with oauth2 type authorization.
- `openIdConnectUrl`: Used with openIdConnect type authorization.

* Required


```javascript
securitySchemes:

    Mashape-Key:
      type: apiKey
      description: "The API authorizes requests through an API key in your header. Enter your Mashape key here. "
      name: X-Mashape-Key
      in: header

    OAuth-key:
        type: oauth2
            flows:
                implicit:
                    authorizationUrl: https://example.com/api/oauth/dialog
                    scopes:
                        write:pets: modify pets in your account
                        read:pets: read your pets
```