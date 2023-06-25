# 0x0B. SSH

## Description

This repository contains solutions to the tasks related to SSH in the ALX System Engineering & DevOps curriculum. The tasks involve configuring SSH, creating SSH key pairs, and connecting to remote servers using SSH.

## Learning Objectives

- Understanding the concept of a server and its typical location.
- Knowledge of SSH and its advantages.
- Creating an SSH RSA key pair.
- Connecting to a remote host using an SSH RSA key pair.
- Understanding the use of `#!/usr/bin/env bash` instead of `/bin/bash`.

## Files

The following are the files present in this repository:

### 0-use_a_private_key

Bash script that connects to a server using the private key `~/.ssh/school` with the user `ubuntu`. The script uses the `ssh` command with single-character flags and does not handle the case of a private key protected by a passphrase.

### 1-create_ssh_key_pair

Bash script that creates an RSA key pair. The private key is named `school` and has a length of 4096 bits. The private key is protected by the passphrase "betty". The script generates the private and public key files.

### 2-ssh_config

This file contains the SSH client configuration required for connecting to a server without typing a password. The configuration specifies the use of the private key `~/.ssh/school` and refuses authentication using a password.

### 3-ssh_key

SSH public key that can be added to a server to allow connection using the `ubuntu` user. This key enables remote access for evaluation purposes.

### 100-puppet_ssh_config.pp

Puppet manifest file that sets up the SSH client configuration file to connect without typing a password. It configures the use of the private key `~/.ssh/school` and refuses authentication using a password

3. Execute the desired script or use the provided files for configuration.

## Credits

This repository contains solutions to tasks on SSH as part of the ALX System Engineering & DevOps curriculum. The curriculum was designed by Sylvain Kalache and all rights are reserved.

This project was completed in collaboration with a team of software engineering students at ALX.
