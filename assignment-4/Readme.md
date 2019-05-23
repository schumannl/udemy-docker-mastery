# HTTPD container with custom default page

### Purpose
To practice image creation

### Build command
```
docker build --tag httpd-with-custom-default-page .
```

### Publish commands
```
docker image tag httpd-with-custom-default-page lmintlaszlo/httpd-with-custom-default-page
docker login
docker push lmintlaszlo/httpd-with-custom-default-page
```

### Run the image
```
docker container run --publish 8080:80 lmintlaszlo/httpd-with-custom-default-page
```
