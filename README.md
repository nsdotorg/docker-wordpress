# docker-wordpress

### Steps to run the application
1. Install `docker` on your machine
2. Run `docker-compose up -d`
3. Open `http://localhost:8000`

### Steps to check mysql tables
1. Run `docker inspect <mysql_container_name>`
2. Run `brew install mysql`
3. Run `brew services start mysql`
4. You can perform a query using the following command
  - `docker exec <mysql_container_name> mysql -u<username> -p<password> -e 'show databases'`
