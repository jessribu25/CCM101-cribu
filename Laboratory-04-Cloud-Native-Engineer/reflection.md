# Mission 4 Reflection

Deploying an application using Docker is much faster than creating a Virtual Machine (VM). Setting up a VM requires installing an operating system, assigning virtual hardware, and waiting for the system to start before installing an application. With Docker, using `docker run` on an image that has already been downloaded can start a container within seconds. This is because containers share the host system's kernel and only run the required application instead of a complete operating system.

Port mapping such as `-p 8080:80` is important because containers have their own isolated network by default. Nginx runs on port 80 inside the container, but it cannot be accessed directly from the host without mapping the port. By connecting host port 8080 to container port 80, users can access the Nginx web server through `localhost:8080`.

Using `docker rm` removes the container and the data stored in its writable layer. This shows why containers are considered temporary or ephemeral. If data needs to remain available even after a container is removed, Docker volumes or bind mounts should be used because they store data separately from the container.

Containerization also improves collaboration between developers and IT teams by reducing the common "it works on my machine" issue. Since the application and its required dependencies can be packaged together inside a container, the same setup can be used during development, testing, and production. This makes deployment more consistent and helps connect software development with IT operations, which is an important part of modern DevOps.

My GitHub portfolio is gradually becoming a collection of practical cloud-related skills instead of only theoretical knowledge. Each laboratory activity introduces a new concept, starting with basic cloud computing and progressing to infrastructure, multi-cloud platforms, and container technologies. Together, these activities show my progress and growing understanding of cloud-native environments.
