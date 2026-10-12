## Laboratory Activity 7: Mission 7 – The Cloud Operations Engineer

Mission Overview
This lab is about observability. It covers checking the health of a host server, deploying a containerized Nginx web server, sending both normal and faulty requests to it, and using Docker's logging and metrics tools to show that the infrastructure is healthy and ready for a surge in traffic.

Objectives
   * Use built-in Linux command-line tools to keep track of host CPU, memory, and disk capacity
   * Launch a web container and watch its performance in real time
   * Send web traffic to the server and pull out the access logs for review
   * Turn raw performance data into a clear, readable technical report

Monitoring Commands Executed
   * `free -h`: shows how much memory is in use and available
   * `df -h`: shows disk storage usage per file system
   * `top`: displays live CPU load and the processes currently running
   * `docker run -d --name client-website -p 8080:80 nginx`: starts the Nginx web container in the background
   * `curl http://localhost:8080`: sends a normal request to mimic regular traffic
   * `curl http://localhost:8080/hidden-admin-page`: sends a request to a nonexistent page to trigger an error
   * `docker logs client-website`: retrieves the container's application logs
   * `docker stats`: shows live resource usage for the container

Skills Learned
   * Setting a host-level performance baseline before anything is deployed
   * Producing and interpreting HTTP access logs, including error status codes
   * Reading live container metrics such as CPU, memory, and network I/O
   * Telling apart monitoring (metrics that show system health over time) from logging (records of individual events)
