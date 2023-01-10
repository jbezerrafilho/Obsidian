******


```Bash
# Criamos um container que rodará o SGBD MySQL

$ docker run --name db-mysql --network=db -p 3306:3306 \
	-e MYSQL_ROOT_PASSWORD=root \
	-v /Users/jbezerra/www/databases/mysql:/var/lib/mysql -d mysql:8.0

# Como boa prática, recomenda-se criar outra instância para acessar a linha de comando.

$ docker run -it --network=db  --rm mysql:8.0 mysql -h db-mysql -u root -p 


```

^837448



