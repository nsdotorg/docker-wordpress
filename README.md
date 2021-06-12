# docker-wordpress

### Steps to run the application
1. Install `docker` on your machine
2. Run `docker-compose up -d`
3. Open `http://localhost:8000`

### Steps to perform a query
1. Run `brew install mysql`
2. Run `brew services start mysql`
3. Query the db instance running in the container using the following command
```shell
# replace "show databases" with any query
docker exec <mysql_container_name> mysql -u<username> -p<password> -e 'show databases'

# club queries together to get the data you need
docker exec <mysql_container_name> mysql -u<username> -p<password> -e 'show databases; use wordpress; SHOW TABLES'
```
4. Run `docker exec -it <mysql_container_name> mysql -u<username> -p<password>` to run queries inside the db instance
```mysql
# example commands to run inside db mysql instance (always add ';' at then end of each command
mysql> use wordpress;
mysql> SHOW TABLES;
mysql> SELECT * FROM wp_options;
```
5. Start/Stop containers as and when required
```shell
# when only wordpress and mysql containers are running
docker container start $(docker container ls -aq)
docker container stop $(docker container ls -aq)

# when other containers are also running
docker container start <wordpress_container_name> <mysql_container_name>
docker container stop <wordpress_container_name> <mysql_container_name>
```
