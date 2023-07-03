Project Overview:

    Objective: Improve the web stack by adding redundancy to the web servers using a load balancer.
    Benefit: Allows handling more traffic and increases infrastructure reliability.

Resources:

    Load balancer introduction and HAProxy information.
    HTTP header explanation.
    HAProxy packages for Debian/Ubuntu.

Tasks:
a. Task 0: Double the number of webservers

    Configure web-02 to be identical to web-01.
    Add a custom Nginx response header (X-Served-By) on both web-01 and web-02.
    Write a Bash script (0-custom_http_response_header) to configure a new Ubuntu machine to fulfill the task requirements.

b. Task 1: Install your load balancer

    Install and configure HAProxy on the lb-01 server.
    Configure HAProxy to distribute traffic to web-01 and web-02 using a round-robin algorithm.
    Ensure HAProxy can be managed via an init script.
    Write a Bash script (1-install_load_balancer) to configure a new Ubuntu machine to fulfill the task requirements.

c. Task 2: Add a custom HTTP header with Puppet (Advanced)

    Automate the creation of a custom HTTP header response using Puppet.
    The custom HTTP header should be named X-Served-By, with the value being the hostname of the Nginx server.
    Write a Puppet manifest (2-puppet_custom_http_response_header.pp) to configure a new Ubuntu machine to fulfill the task requirements
