## **Docker-BootCamp**
### **Prepared By : Chandan Chaudhari**
---
### Docker Introduction:
Docker is an open-source platform that allows developers to build, package, and run applications inside lightweight containers.

A container is a standardized unit that contains:

1. Application code

2. Dependencies (libraries, runtime, system tools)

3. Configurations

This makes the application portable, meaning it runs the same way on any system — whether it’s your laptop, a server, or the cloud.

---
1. Once Docker Installed on Windows Operating System
Docker --version

---
2. Check Docker Information
Docker info

---
3. Working with Images
docker search <image>            # Search for an image on Docker Hub
docker pull <image>              # Download image from Docker Hub
docker images                    # List all images
docker rmi <image_id>            # Remove an image
docker history <image>           # Show image history

---
4. Working with Containers
docker run <image>                       # Run container from image
docker run -it <image> bash              # Run container in interactive terminal
docker run -d <image>                    # Run container in background (detached mode)
docker ps                                # List running containers
docker ps -a                             # List all containers (including stopped)
docker stop <container_id>               # Stop container
docker start <container_id>              # Start container
docker restart <container_id>            # Restart container
docker rm <container_id>                 # Remove container
docker logs <container_id>               # View container logs
docker exec -it <container_id> bash      # Access running container shell

---
5. Containers and Image Management
docker inspect <container_id>       # Detailed info about container
docker stats                        # Real-time resource usage
docker top <container_id>           # Show processes inside container
docker diff <container_id>          # Show changes in container filesystem
docker cp <container_id>:<path> .   # Copy files from container to host

---
6. Build Image with Docker File
docker build -t <image_name> .      # Build image from Dockerfile
docker tag <image_id> user/repo:tag # Tag image
docker push user/repo:tag           # Push image to Docker Hub

---
7. Docker Volume
docker volume create mydata         # Create volume
docker volume ls                    # List volumes
docker run -v mydata:/data ubuntu   # Mount volume to container
docker volume rm mydata             # Remove volume

---
8. Docker Networks
docker network ls                   # List networks
docker network create mynetwork     # Create custom network
docker network connect mynetwork <container>  # Connect container
docker network inspect mynetwork    # Inspect network details

---
9. Cleanup Commands
docker system prune                 # Remove unused data
docker image prune                  # Remove unused images
docker container prune              # Remove stopped containers
docker volume prune                 # Remove unused volumes

---