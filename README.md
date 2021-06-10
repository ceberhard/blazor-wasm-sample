# blazor-wasm-sample

Database Setup

`docker pull mysql/mysql-server:latest`

`docker run --name=blazorSQL -d mysql/mysql-server:latest`

Then review the logs in Docker Desktop or through the `docker logs blazorSQL` for the `GENERATED ROOT PASSWORD: [pword]` statement. Use that password when running the next command. 

`docker exec -it blazorSQL mysql -uroot -p`
