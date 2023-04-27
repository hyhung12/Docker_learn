# Docker_learn

- Why Docker?
+ Install software easily w/o set up dependencies

- Image: single file + config required to run a program
- Container (program): instance of image, has its own memory
+ a running process with computer resources

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
