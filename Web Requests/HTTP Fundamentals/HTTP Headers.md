Headers are dividedinto following categories:
1. General Headers
2. Entity Headers
3. Request Headers
4. Response Headers
5. Security Headers

## General Headers
Used to describe the `context`
1. **Date**: Also includes time and day.
2. **Connection:** Should the connection stay alive after request finishes? Common values are `close` and `keep-alive` 

## Entity Headers
Used to describe the content tranferred.
==Note: Usually found in POST or PUT requests.==

1. **Content-Type**: e.g text/html or application/json, **Syntax:** type/subtype/parameters ( like charset=UTF-8) 
2. **Boundary** : Separate content when there is more than one in the same message. e.g form data
3. **Content-Length**
4. **Content-Encoding**: *exists to tell the receiver how to decode the message body to its original format*
## Request Headers
Used to give info about the request and the client

### Function:
**Provide more information about the request context**, make the *request conditional* based on the *target resource state*, suggest *preferred formats* for the response,supply *authentication credentials*.

**Full info**: https://tools.ietf.org/html/rfc7231#section-5

