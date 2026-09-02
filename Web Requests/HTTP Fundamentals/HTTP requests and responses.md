**Note:** There is always a respone to a request, but existence of response data depends on requester access rights.

## HTTP request format

![[Pasted image 20260902143730.png]]

 %%headers are terminated with a new line, which is necessary for the server to validate the request.%%

HTTP version 2.X sends request as binary data in dictionary form

Finally, a request may end with the request body and data.
## HTTP Response format
![[Pasted image 20260902144645.png]]

curl -v flag give details usefull for pentration test or exploits.

Using curl by default sends a GET request.

# DevTools

Our concern is in network tab to look for exploits and vulnarabilities.