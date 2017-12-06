
# OpenApi Specification


The schema exposes two types of fields.

- Fixed fields, which have a declared name
- Patterned fields, which declare a regular expression pattern for the field name.

### File Structure

The OAS representation of the API is made of a single file. However, parts of the definitions can be split into separate files, at the discretion of the user. This is applicable for $ref fields in the specification as follows from the JSON Schema definitions.

By convention, it is RECOMMENDED that the OpenAPI Specification (OAS) file be named openapi.json or openapi.yaml.

## Data Types




Common Name | [`type`](#dataTypeType) | [`format`](#dataTypeFormat) | Comments
----------- | ------ | -------- | --------
integer | `integer` | `int32` | signed 32 bits
long | `integer` | `int64` | signed 64 bits
float | `number` | `float` | |
double | `number` | `double` | |
string | `string` | | |
byte | `string` | `byte` | base64 encoded characters
binary | `string` | `binary` | any sequence of octets
boolean | `boolean` | | |
date | `string` | `date` | As defined by `full-date` - [RFC3339](http://xml2rfc.ietf.org/public/rfc/html/rfc3339.html#anchor14)
dateTime | `string` | `date-time` | As defined by `date-time` - [RFC3339](http://xml2rfc.ietf.org/public/rfc/html/rfc3339.html#anchor14)
password | `string` | `password` | Used to hint UIs the input needs to be obscured.