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
# example command to run inside db mysql instance
use wordpress; SHOW TABLES; SELECT * FROM wp_options;
```
