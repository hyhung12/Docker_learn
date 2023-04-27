# Docker_learn

- Why Docker?
+ Install software easily w/o set up dependencies

- Image (blueprint): read-only file that contains all the necessary components to run an application
- Container (program): lightweight, isolated environment that includes all the necessary components

Docker: Client (take our cmd), Server, Hub(has free image)

```
docker ps
docker ps -all (show all contaners that have been created)
docker run = docker create + docker start
```
```
docker create hello-world (create a container from the hello-world image)
docker start -a <container-id>
```
- To start a container that has already exited
```
docker start -a <container-id>
docker system prune
