# Dealing with swarm

### Initializing swarm
```
docker swarm init
```

### Creating an Alpine service
```
docker service create alpine ping 8.8.8.8
```

### Listing services
```
docker service list
```

### Adding replicas to the service
```
docker service update modest_newton --replicas 2
```

### Removing a service
```
docker service rm modest_newton
```

### Leaving swarm
```
docker swarm leave --force
```