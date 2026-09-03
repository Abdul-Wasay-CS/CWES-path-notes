**Website to monitor**: https://github.com/Abdul-Wasay-CS/CWES-path-notes

**For a page that uses basic auth:**
- Use `curl -u username:password http://<server_ip>:<port>/`  
- **another method**: `curl http://username:password@<server_ip>:<port>/`
- We can also manually add header using -H:
	- eg for admin:admin , encrypted basic auth is *YWRtaW46YWRtaW4=*
	- the request can be authorized by:
		- `curl -H "Authorization: Basic YWRtaW46YWRtaW4=" http://154.57.164.73:30736`

The authentication can be maintained for future requests using cookies.

