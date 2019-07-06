# Testing bind mounts

### Bind mounting htdocs from host to container
```
docker container run --detach --publish 8080:80 --volume %cd%\htdocs:/usr/local/apache2/htdocs httpd:2.4
```
