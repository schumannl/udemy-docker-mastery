# Managing multiple containers

### Starting containers
```
docker container run --detach --name nginx --port 8080:80 nginx
docker container run --detach --name httpd --port 8181:80 httpd
docker container run --detach --name mysql --publish 3306:3306 --env MYSQL_RANDOM_ROOT_PASSWORD=1 mysql:5.7
```

### Searching root password
```
docker container logs mysql
```

### Listing containers
```
docker container list
```

### Stopping containers
```
docker container stop nginx httpd mysql
```

### Removing containers
##### Solution 1
```
docker container rm nginx httpd mysql
```
##### Solution 2
```
docker container prune
```
