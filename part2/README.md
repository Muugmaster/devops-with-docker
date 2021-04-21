# 2.1

[Docker-compose.yml](./2.1/docker-compose.yml)

```sh
# Run on same folder where this docker-compose.yml is:
mkdir logs && touch logs/text.log
# Then run docker-compose
docker-compose up
```

# 2.2

[Docker-compose.yml](./2.2/docker-compose.yml)

# 2.3

[Docker-compose.yml](./2.3/docker-compose.yml)

# 2.4

[Used same containers what were created in 1.14](../part1/1.14)

[Docker-compose.yml](./2.4/docker-compose.yml)

# 2.5

```sh
docker-compose up -d --scale compute=3
```

# 2.6

[Used same containers what were created in 1.14](../part1/1.14)

[Docker-compose.yml](./2.6/docker-compose.yml)

# 2.7

[Docker-compose.yml](./2.7/docker-compose.yml)

# 2.8

[Docker-compose.yml](./2.8/docker-compose.yml)

[nginx.conf](./2.8/nginx.conf)

# 2.9

[Docker-compose.yml](./2.9/docker-compose.yml)

# 2.10

[Frontend Dockerfile](./2.10/frontend/Dockerfile)

[Backend Dockerfile](./2.10/backend/Dockerfile)

[Docker-compose.yml](./2.10/docker-compose.yml)

# 2.11

I have been using for my own projects database images from docker ie. mongodb and postgresql. Its easier to run databases in containers when developing than always installing them locally or tryin to use some free cloud provider for database.

[Here](https://github.com/Muugmaster/jasenrekisteri-mern) is one older project of mine where I added in README a docker command to use so you get mongodb running and introduction how to get connectod to that mongodb running in container. 

But im pretty sure after this course im gonna try to implement more docker in my develop enviroment.