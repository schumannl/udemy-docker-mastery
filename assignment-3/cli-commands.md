# DNS round robin testing

### Creating the new network
```
docker network create dns-rr
```

### Starting ElasticSearch containers
```
docker container run --detach --name elastic1 --network dns-rr --network-alias dns-rr-alias elasticsearch:2
docker container run --detach --name elastic2 --network dns-rr --network-alias dns-rr-alias elasticsearch:2
```

### Checking aliases with Alpine
```
docker container run --rm --network dns-rr alpine nslookup dns-rr-alias
```

### Checking responses with CentOs
```
docker container run --rm --network dns-rr centos curl -s dns-rr-alias:9200
```