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

### Path 

Holds the relative paths to the individual endpoints and their operations.

### Path Fields

- `path` * : A relative path to an individual endpoint 

### Paths at the root Level
```javascript
paths:
  /posts:
    get:

  /posts:
    post:

  /posts:
    put:

  /posts:
    delete:
```
