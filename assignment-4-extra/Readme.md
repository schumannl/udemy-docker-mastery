# HTTPD with MC

### Purpose
To practice image creation

### Build command
```
docker build --tag httpd-with-mc .
```

### Publish commands
```
docker image tag httpd-with-mc lmintlaszlo/httpd-with-mc
docker login
docker push lmintlaszlo/httpd-with-mc
```

### Run the image
```
docker container run -it --rm lmintlaszlo/httpd-with-mc mc
```