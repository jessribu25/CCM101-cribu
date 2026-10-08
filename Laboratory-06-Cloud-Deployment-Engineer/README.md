# Laboratory Activity 6: Mission 6 – The Cloud Deployment Engineer

## Mission Overview

This laboratory activity introduces the concept of Infrastructure as Code (IaC) through Docker Compose. The task involves deploying a two-tier private cloud storage system using Nextcloud and MariaDB. Instead of creating and configuring each container manually, a single YAML file is used to define and deploy the entire application.

## Objectives

* Understand the basic structure of a multi-tier application
* Learn the purpose and organization of a `docker-compose.yml` file
* Use the `nano` editor to create configuration files through the command line
* Deploy multiple containers using Docker Compose
* Record the deployment process and understand the principles of Infrastructure as Code

## Commands Executed

* `mkdir nextcloud-deployment` and `cd nextcloud-deployment`
* `nano docker-compose.yml`
* `docker-compose up -d`
* `docker-compose ps`
* `docker-compose down`

## Skills Learned

* Creating properly structured and correctly indented YAML configuration files
* Deploying multiple connected containers using a single command
* Understanding how Docker Compose provides internal networking and DNS, allowing containers to communicate using their service names
* Creating clear Infrastructure as Code documentation that can be easily understood and reused by other engineers
