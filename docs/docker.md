#### **Lifecycle Commands**

*   `docker create [image]`: Create a new container from an image
*   `docker run [image]`: Create and start a container
*   `docker start [container]`: Start one or more stopped containers
*   `docker stop [container]`: Stop one or more running containers
*   `docker rm [container]`: Remove one or more containers

#### **Inspecting & Managing**

*   `docker ps`: List running containers
*   `docker ps -a`: List all containers (running and stopped)
*   `docker images`: List all images
*   `docker logs [container]`: Fetch the logs of a container
*   `docker exec -it [container] [command]`: Run a command in a running container

#### **Image Management**

*   `docker build -t [name] .`: Build an image from a Dockerfile
*   `docker pull [image]`: Pull an image from a registry
*   `docker push [image]`: Push an image to a registry
*   `docker rmi [image]`: Remove one or more images
