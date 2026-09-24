## MySQL

Pull MySQL image:

docker pull khrystyna079/mysql-local:1.0.0

Create volume:

docker volume create mysql_data

Run MySQL container:

docker run -d \
  --name mysql-todo \
  -v mysql_data:/var/lib/mysql \
  -p 3306:3306 \
  khrystyna079/mysql-local:1.0.0


## Application

Pull application image:

docker pull khrystyna079/todoapp:2.0.0

Run application container:

docker run -d \
  --name todoapp \
  -p 8080:8080 \
  khrystyna079/todoapp:2.0.0

## Browser

Open the application in a browser:

http://localhost:8080

API:

http://localhost:8080/api/

## Docker Hub

https://hub.docker.com/repository/docker/khrystyna079/todoapp/