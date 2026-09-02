Essential tool to send web requests from command line . Is also great for automation by using it in scripts.

# Usage
To send an HTTP request to first website:
`CallEntropy@htb[/htb]$ curl http://info.cern.ch/` 

The request can be sent to an ip aswell like:
`curl -O 154.57.164.82:31600/download.php`
## Flags
To download a page or file use -O flag.
-o flag requires new file name.
-O flag uses the same file name as the server.
E.g
`CallEntropy@htb[/htb]$ curl -O http://info.cern.ch/index.html`

Use `-s` flag doesnt print status white processing the request.
Use -h flag to see other options.
For all  options: Use `man curl` or `curl --help all`

**Difference from Browser:** Instead of rendering the code like browsers, it prints it in raw format

Our interest is the request and respone context not the output which cURL helps finding it faster and more convenient.
# Request and Response Context
- **The Web Request Context:** The request context includes everything the server needs to know about what the client wants and who is asking. 
- **The Web Response Context:** The response context includes everything the server sends back after processing the request. 
