# CLI testing containers

### Starting CentOs container
```
docker container run --rm -it --name centos centos:7 bash
```

### Updating CURL in CentOs container
```
yum update curl
```

### Starting Ubuntu container
```
docker container run --rm -it --name ubuntu ubuntu bash
```

### Updating CURL in Ubuntu container
```
apt-get update && apt-get install curl
```