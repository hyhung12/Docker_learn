# Docker_learn

- Docker -> Install software easily w/o set up dependencies
- Image (blueprint): read-only file that contains all the necessary components to run an application
- Container (program): lightweight, isolated environment that includes all the necessary components

![](https://github.com/hyhung12/Docker_learn/blob/main/docker0.png)
![](https://github.com/hyhung12/Docker_learn/blob/main/docker2.png)


Docker: Client (take our cmd), Server, Hub(has free image)
- Create a container from image
```
docker run hello-world
// docker run = docker create + docker start
```
![](https://github.com/hyhung12/Docker_learn/blob/main/docker1.png)

| **Command** | **Description** |
|-|-|
| docker run hello-world | create a container from image |
| docker ps | show all contaners that are running |
| docker ps -all | show all contaners |
| docker create hello-world  | create a container |
| docker start -a "container-id"  | start a container |
| docker system prune | remove unused all containers & images  |
| docker stop/kill "container-id"  | stopping containers |
| docker system prune | remove unused all containers & images  |
| docker exec -it "container-id" | **run additional command in a container** |
| docker exec -it "container-id" sh ||
| -i: take input of terminal ||
| -t: same as prettier  ||

## Dockerfile
![](https://github.com/hyhung12/Docker_learn/blob/main/dockerfile0.png)
- Alpine as base image: has preinstalled set of programs
```
FROM alpine / FROM node:14-alpine
RUN apk add --update redis / RUN npm install
CMD ["redis-server"] / CMD ["npm", "start"]
```

```
docker build -t usrn/app_folder .
docker run -p 3000:8080 ayya/simple
docker run -it usrn/app_folder sh
```

| Option | Description |
|-|-|
| docker-compose up | start the containers and network |
| docker-compose up --build | use Dockerfile to re-build image then start (for changes) |
| docker-compose up -d  | run in detached mode (container run in background -> using terminal w/o being blocked) |
| docker-compose down | stop containers |
|||
|  ||
|  ||


- Restart policy
- Flow: Developing -> Testing -> Deploying
- Docker volume: map folder
- Travis pull code if it detects change in GitHub repo
