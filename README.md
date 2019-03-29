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

start the containers

`$ docker-compose up -d`

access the midpoint server at `https://localhost`