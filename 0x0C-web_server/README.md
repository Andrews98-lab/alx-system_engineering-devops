# 0x0C. Web server

## Description
This project focuses on configuring and managing a web server. The tasks involve automating the setup and configuration process using Bash scripts and Puppet manifests. The main objective is to learn about web servers, their role, DNS, DNS record types, and HTTP requests.

## Concepts
- Child Process: Understanding the concept of child processes and their role in web servers.

## Tasks
### 0. Transfer a file to your server
Write a Bash script that transfers a file from a client machine to a server using `scp`.

### 1. Install nginx web server
Write a Bash script that installs and configures Nginx web server on a server.

### 2. Setup a domain name
Configure the DNS records for a domain name, pointing the root domain to the web server's IP address.

### 3. Redirection
Configure Nginx to redirect a specific path to another page using a "301 Moved Permanently" redirect.

### 4. Not found page 404
Configure Nginx to display a custom 404 page when a requested page is not found.

### 5. Install Nginx web server (w/ Puppet)
Write a Puppet manifest to install and configure Nginx web server, including the redirection setup.

