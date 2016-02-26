# Docker DynamoDB
A very basic Docker DynamoDB container based heavily on the work by ryanratcliff.

### To build the container
```
docker build -t savaki/dynamodb .
```

### Alternatively, the container can be pulled from Docker Registry
```
docker pull savaki/dynamodb
```

# Exposed Endpoints
The dynamodb local jar besides providing a dynamodb setup for development purposes also exposes a javascript shell for managing the tables

### If ports are exposed
```
http://localhost:8000/shell
```

### Direct connection to container
```
http://my_dynamodb_container:8000/shell
```

# Example usages

### To startup as is
```
docker run -d savaki/dynamodb
```

### To startup with all ports exposed to host
```
docker run -d -P savaki/dynamodb
```

### To startup with specific port exposed
```
docker run -d -p 8000:8000 savaki/dynamodb
```
