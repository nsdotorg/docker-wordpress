# docker-wordpress

### Steps to run the application
1. Install `docker` on your machine
2. Run `docker-compose up -d`
3. Open `http://localhost:8000`

### Steps to perform a query
1. Run `brew install mysql`
2. Run `brew services start mysql`
3. You can perform a query using the following command
  - `docker exec <mysql_container_name> mysql -u<username> -p<password> -e 'show databases'`
