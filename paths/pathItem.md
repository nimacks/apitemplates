# Open Api Specification 

## Path Item

Holds the relative paths to the individual endpoints and their operations.

  
#### Path Item Fields
- `$ref` : allows for external definition of this path item 
- `summary`: optional string summary
- `description`: optional string description
- `get` : a defintion of a GET operation on this path ([`operation object`]())
- `put` : a defintion of a POST operation on this path ([`operation object`]())
- `post` : a defintion of a POST operation on this path ([`operation object`]())
- `delete` : a defintion of a DELETE operation on this path ([`operation object`]())
- `options` : a defintion of a OPTIONS operation on this path ([`operation object`]())
- `head` : a defintion of a HEAD operation on this path ([`operation object`]())
- `patch` : a defintion of a PATCH operation on this path ([`operation object`]())
-  `trace` : a defintion of a Trace operation on this path ([`operation object`]())
-  `servers` : an alternative server array to service all operations in this path ([`server object`]())
-  `parameters`: a list of all parameters that are applicable for all the operations described under this path ([`parameter object` |`reference object`]())



### Paths at the root Level
```javascript
paths:
  /posts:
    get:
      tags:
      - Post Information
      summary: getPosts
      description: Gets all posts
      operationId: GetPosts
      externalDocs:
        description: More Details
        url: 'http://example.com'
      parameters:
        
      responses:
      deprecated:
      security:
      servers:
      requestBody:
      callbacks:

  /posts:
    Post:
      tags:
      summary:
      description:
      operationId:
      externalDocs:
      parameters:
      responses:
      deprecated:
      security:
      servers:
      requestBody:
      callbacks:


```
