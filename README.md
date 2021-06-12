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
```
