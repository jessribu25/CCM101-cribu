# Laboratory Activity 8: Mission 8 – The Cloud Security Engineer

## Mission Overview
This lab puts defense-in-depth into practice by securing a live server with a host-based firewall. It involves deploying a publicly exposed web application, auditing which ports are open, and setting up UFW with a Default Deny policy so that only the services the application truly requires can receive traffic.

## Objectives
- Explain the attack surface and the Principle of Least Privilege
- Carry out a basic security audit of active network ports
- Set up UFW with a Default Deny policy
- Apply granular port management for SSH and HTTP traffic

## Commands Executed
- `docker run -d --name secure-web-app -p 8080:80 nginx`: launched the exposed web application
- `sudo ufw allow ssh`: permitted SSH before the firewall was turned on
- `sudo ufw default deny incoming` / `sudo ufw default allow outgoing`: established the Default Deny policy
- `sudo ufw enable`: switched the firewall on
- `sudo ufw status verbose`: checked that the rules were active
- `sudo ufw allow 8080/tcp`: opened the port the web application uses
- `sudo ufw status numbered`: confirmed the new rule was in place

## Skills Learned
- Setting up a host-based firewall with a Default Deny policy
- Recognizing why the order of steps matters, such as allowing SSH before enabling the firewall
- Managing ports at a granular level to keep a server's attack surface small
- Writing clear security documentation that other engineers can follow
