# Laboratory 04: Cloud-Native Engineer

## Mission Overview
This lab covers the transition from traditional Virtual Machines to containerized applications using Docker. It includes researching VM vs. container architecture, deploying a live Nginx container, and managing its lifecycle.

## Objectives
- Differentiate between VMs and Containers
- Access a Docker-enabled environment using KillerCoda
- Execute fundamental Docker CLI commands
- Pull, run, manage, and terminate a containerized application (Nginx)
- Document container operations in Markdown

## Docker Commands Executed
```bash
docker --version
docker info
docker pull nginx
docker run -d -p 8080:80 --name my-nginx nginx
curl http://localhost:8080
docker ps
docker stop my-nginx
docker ps -a
docker rm my-nginx
```

## Skills Learned
- Verifying a Docker environment's installation and status
- Pulling images from Docker Hub
- Running containers in detached mode with port mapping
- Managing the full container lifecycle (list, stop, verify, remove)

## Challenges Encountered
*(Fill this in with anything that actually tripped you up — e.g., port already in use, forgetting `-d`, container name conflicts, etc.)*
