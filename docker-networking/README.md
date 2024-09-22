# Docker Network 

```
docker run -d --name login nginx:latest
    docker exec -it login /bin/bash

    apt-get install iputils-ping -y

    ping -V
```

- in a new terminal 

```
docker run -d --name logout nginx:latest

docker ps

docker inspect login 
```

- copy ipaddress of logout

```
    #and inside login container or previous terminal 
    ping <ipaddress of logout container>
```

# create a docker network 

```
docker network create secure-network

docker network ls

docker run -d --name finance --network=secure-network nginx:latest
```

- now you will not be able to connect finance container through other container 