# Updating database with named volumes

### Creating volume
```
docker volume create --name database
```

### Binding volume to a MySQL 5.7 container
```
docker container run --name database --env MYSQL_ALLOW_EMPTY_PASSWORD=1 --volume database:/var/lib/mysql mysql:5.7
```

### Adding changes to the volume
```
docker container exec -it database mysql
mysql> CREATE DATABASE `test`;
```

### Exchanging containers over volume
```
docker container stop database
docker container rm database
docker container run --name database2 --env MYSQL_ALLOW_EMPTY_PASSWORD=1 --volume database:/var/lib/mysql mysql:5.7
```

### Checking previous changes
```
docker container exec -it database2 mysql
mysql>  show databases;
```

### Voilà :)
```
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| test               |
+--------------------+
5 rows in set (0.00 sec)

```
