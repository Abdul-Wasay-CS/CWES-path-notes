# Important:

You can double click the request name in devtools to see what request was made.

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

**Referer:** Can be easily manipulated, isnt to be trusted.
**Cookie:** Contains client side data to identify user on the server.

**Full info**: https://tools.ietf.org/html/rfc7231#section-5

## Response Headers

1. server
2. **Set-cookie**: client's identifier for future requests.
3. www-Authenticate
## Security Headers
1. **Content-Security-Policy:**  Website's policy toward externally injected scipts
2. **Strict-Transport-Securtiy:** Force HTTPS:// to prevent stolen information.
3. **Referrer-Policy**: Whether the browser will set the value for refferer or not.

**Full List of all headers**: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers

## Curl

-H flag can be used to set request headers.
e.g -A "[user-agent-name]" can be used change our user-agent to literally  anything.

