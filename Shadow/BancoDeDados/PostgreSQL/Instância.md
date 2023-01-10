----
#postgresql

```shell
$ docker network create db 
$ mkdir db-data 
$ cd db-data

$ docker run --name db -p 5432:5432 --network=db \
	-v "$PWD:/var/lib/postgresql/data" -e POSTGRES_PASSWORD=password \
	-d postgres:15.1-alpine

$ docker run -it --rm --network=db postgres:15.1-alpine \
	psql -h db -U postgres
```

