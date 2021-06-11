# blazor-wasm-sample

Database Setup

`docker pull mysql/mysql-server:latest`

`docker run -p 3307:3306 --name=blazorSQL -e MYSQL_ROOT_PASSWORD=[my_password_here] -d mysql/mysql-server:latest`

Then review the logs in Docker Desktop or through the `docker logs blazorSQL` for the `GENERATED ROOT PASSWORD: [pword]` statement. Use that password when running the next command. 

`docker exec -it blazorSQL mysql -uroot -p`

Then enter the root password.

At the `mysql>` prompt:

`CREATE USER 'admin'@'%' IDENTIFIED BY '[admin_password_here]';`

`GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%';`

You should then be able connect to the mySQL database via MySQL WorkBench:
  - **Hostname**:  `localhost`
  - **Post**: `3307`
  - **Username**: `admin`
