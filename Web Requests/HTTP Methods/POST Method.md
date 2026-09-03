**HTTP `POST` places user parameters within the HTTP Request body instead of URL for the following reasons:**
- Large files, which would be inefficeint to log as part of URL ( takes shit ton of space ).
- URL need to have characters that can be converted to letter. Post puts the data in binary so its easier to put it in body.
- URL has a character limit, but body doesnt, so large files can be transferred.

You can just check data sent in POST using request tab in the network devtool.
![[Pasted image 20260903152416.png]]

cURL -X is used to specify the request method.
then -d is used to specify the parameters
**When using cURL to authenticate:**  Some login forms redirect to seperate page, to follow redirection use `curl -L`

After authenticating once: just use the cookie provided with -b flag for curl.
Getting hands on the cookie can be enough to launch an attack, its known as **Cross Site Scripting**

https://portswigger.net/web-security/cross-site-scripting


An example of using cURL to send a post request to use a cookie on user to login and then search using -d parameters:
`curl -X POST -d '{"search":"flag"}' -b "PHPSESSID=f989gpo8eki1l91857itqlrle8" -H "Content-Type: application/json" http://154.57.164.68:30339/search.php
`
