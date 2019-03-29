Make sure to change the password located in `./configs-and-secrets/midpoint/database_password.txt`

Create a `.env` file like below, modifying any variables needed.

```# These parameters can be overridden by setting environment variables before calling docker-compose up
   ENV=demo
   USERTOKEN=
   REPO_MISSING_SCHEMA_ACTION=create
   REPO_UPGRADEABLE_SCHEMA_ACTION=stop
   MP_MEM_MAX=2048m
   MP_MEM_INIT=1024m
   TIMEZONE=UTC
```
Generate the ssl key/cert for nginx ssl proxy
```
$ openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
   -keyout ./nginx/nginx.key \
   -out ./nginx/nginx.crt
```
Copy the cert to the `midpoint_server/ssl_certs/` directory
```
$ cp ./nginx/nginx.crt ./midpoint_server/ssl_certs/
```

start the containers

`$ docker-compose up -d`

Access midpoint: 

* URL: https://127.0.0.1/midpoint
* username: `Administrator`
* password: `5ecr3t`