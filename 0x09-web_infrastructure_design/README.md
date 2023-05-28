# Web Infrastructure Design

This project focuses on designing various web infrastructure setups to host a website called www.foobar.com. The goal is to understand the components involved, their roles, and the potential issues with each infrastructure design. The project is divided into four tasks, each building upon the previous one to create a more advanced and scalable web infrastructure.

## Task 0: Simple Web Stack

In this task, we design a basic web infrastructure consisting of a single server with a LAMP stack. The components required are as follows:

- 1 server
- 1 web server (Nginx)
- 1 application server
- 1 application files (code base)
- 1 database (MySQL)
- 1 domain name "foobar.com" configured with a "www" record pointing to the server IP (e.g., 8.8.8.8)

To understand this infrastructure, we should be able to explain the following concepts:

- The server: It refers to the physical or virtual machine hosting the web infrastructure.
- The domain name: It is a human-readable address used to access the website.
- DNS record: The "www" record is a DNS record type (CNAME or A) that associates the "www.foobar.com" domain with the server's IP address.
- The web server: It handles incoming HTTP requests and serves static content.
- The application server: It runs the application code and generates dynamic content based on the requests.
- The database: It stores and manages the website's data, such as user information or content.
- Communication: The server uses the network to communicate with the user's computer, typically using the HTTP protocol.

The issues with this infrastructure include:

- Single Point of Failure (SPOF): If the server fails, the entire website becomes inaccessible.
- Downtime during maintenance: When deploying new code, the web server needs to be restarted, causing temporary downtime.
- Limited scalability: The infrastructure cannot handle high traffic loads efficiently.

## Task 1: Distributed Web Infrastructure

In this task, we enhance the web infrastructure by introducing redundancy and load balancing. The components added are:

- 2 servers
- 1 web server (Nginx)
- 1 application server
- 1 load balancer (HAproxy)
- 1 set of application files (code base)
- 1 database (MySQL)

We should be able to explain the following concepts:

- Load balancer: It evenly distributes incoming traffic across multiple servers to improve performance and ensure high availability.
- Distribution algorithm: The load balancer uses a specific algorithm (e.g., round-robin, least connections) to determine how requests are distributed.
- Active-Active vs. Active-Passive setup: In an Active-Active setup, all servers actively handle incoming requests, while in an Active-Passive setup, only one server is actively serving requests while the others remain idle as backups.
- Primary-Replica (Master-Slave) database cluster: It involves having a primary database node for write operations and one or more replica nodes for read operations and data replication.

The issues with this infrastructure include:

- Single Points of Failure (SPOF): If the load balancer or any server fails, the website's availability is affected.
- Security issues: Lack of a firewall and HTTPS encryption can expose the infrastructure to potential threats.
- Lack of monitoring: Without monitoring, it becomes difficult to identify and address issues promptly.

## Task 2: Secured and Monitored Web Infrastructure

In this task, we enhance the web infrastructure by adding security measures and monitoring capabilities. The components added are:

- 3 firewalls
- 1 SSL certificate to serve www.foobar.com over HTTPS
- 3 monitoring clients (data collector for Sum ologic or other monitoring services)

We should be able to explain the following concepts:

- Firewalls: They act as a barrier between the infrastructure and potential threats, monitoring and controlling incoming and outgoing network traffic.
- HTTPS: It is a secure version of the HTTP protocol that encrypts the communication between the server and the user's browser, ensuring data confidentiality and integrity.
- Monitoring: It involves collecting and analyzing data to ensure the infrastructure's performance, availability, and security. Monitoring tools track various metrics and provide insights into system health and potential issues.
- Traffic monitoring: Monitoring tools collect data on various aspects such as response times, error rates, and traffic volume to measure the web server's Quality of Service (QPS).

The issues with this infrastructure include:

- SSL termination at the load balancer level: Termination at the load balancer prevents end-to-end encryption, potentially exposing sensitive data within the infrastructure.
- Single MySQL server accepting writes: Having only one server capable of accepting write operations can become a performance bottleneck and a single point of failure.
- Uniform server components: Having all servers with the same components (database, web server, and application server) might lead to resource inefficiencies and limited flexibility for different workload requirement
