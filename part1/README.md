# 1.1 Getting Started

```sh
docker container run -d nginx <- run 3 times
docker container stop 3c38 2797
docker ps -a
```

![1.1](./images/1.1.png)

# 1.2 Clean Up

```sh
docker container stop 3d8c
docker container rm 2797 3d8e 3c38
docker image rm nginx
```

![1.2](./images/1.2.png)

# 1.3 Secret Message

```sh
docker run -d -it --name secret-msg devopsdockeruh/simple-web-service:ubuntu

docker exec -it secret-msg bash

# Inside container
tail -f ./text.log

# Secret message
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```

![1.3](./images/1.3.png)

# 1.4 Missing dependencies

```sh
docker run -d -it --name website ubuntu sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'

# Go inside ubuntu container to install curl
docker exec -it website bash
# Inside container
apt-get update
apt-get install curl
# Exit container
exit
# Start container
docker start -ai website
input: helsinki.fi
```

![1.4](./images/1.4.png)
