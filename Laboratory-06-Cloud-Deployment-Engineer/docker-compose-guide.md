# Docker Compose Guide — Nextcloud + MariaDB

## What does the `services:` block do?

The `services:` section lists all the containers needed for the application. In this setup, there are two services: `database` and `app`. Each service has its own container, image, environment variables, and configuration. Docker Compose uses this section to create and run all the containers together.

## How did the Nextcloud app container find the database container?

The Nextcloud app connects to the database using the `MYSQL_HOST=database` environment variable. Docker Compose automatically creates a private network for the services and allows them to communicate using their service names as hostnames. Because of this, the `app` container can connect to the database using `database` instead of needing to know its IP address.

## Difference between `docker run` and `docker-compose up -d`

The `docker run` command is normally used to create and start a single container, with its settings provided through command-line options. On the other hand, `docker-compose up -d` uses a YAML configuration file to start all the services defined in it. It automatically handles settings such as networking and environment variables, making it more convenient and less prone to errors when working with multiple containers.
