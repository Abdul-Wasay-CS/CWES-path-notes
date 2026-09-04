CRUD stands for Create, Read, Update, and Delete, 
![[Pasted image 20260903211302.png]]

## Curl get command for CRUD API 

`curl http://<server_id>:<port_id>/<api_name>.php/<table_name>/<search_name>`

**to format the output JSON:** Pipe the command into `jq` a

## Curl Post Command for CRUD API CREATE
```
curl -X POST http://<SERVER_IP>:<PORT>/api.php/city/ -d '{"city_name":"HTB_City", "country_name":"HTB"}' -H 'Content-Type: application/json'
```

### Fetch syntax for POST:
```
await fetch("http://154.57.164.82:30284/api.php/city", {
    "credentials": "include",
    "headers": {
        "User-Agent": "Mozilla/5.0 (X11; Linux x86_64; rv:140.0) Gecko/20100101 Firefox/140.0",
        "Accept": "*/*",
        "Accept-Language": "en-US,en;q=0.5",
        "Content-Type": "application/json",
        "Priority": "u=0, i"
    },
	"body":JSON.stringify({
		"city_name": "Citadel",
		"country_name": "Pharloom"
	}),
    "method": "POST",
    "mode": "cors"
});
```

# CURL Put for CRUD UPDATE
**Depending on the server**: Sometimes if put cant find the record to update, it will create it first and then update it
```
curl -X PUT http://154.57.164.82:30284/api.php/city/london -d '{"city_name":"New_HTB_City", "country_name":"HTB"}' -H 'Content-Type: application/json'

```

PATCH is used when not all fields are to be updated, wheras PUT requires entry for all the fields.

# CURL Delete for CRUD DELETE

Deleting a record removes all instances matching the searched word.
if there are two cities named Citadel, and we use delete for city/Citadel
it will remove both cities.