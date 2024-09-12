# Environment Setup Script for Ubuntu 24

This Bash script simplifies server setup by automating the installation of Nginx, PHP 8.3, MySQL, Node.js (LTS), Composer, Redis, and Supervisor, all in one go. It also generates an SSH key for GitHub, making it especially useful for Laravel developers.

## Features
- **Installs and configures:**
  - **Nginx** – A powerful web server.
  - **PHP 8.3** – Latest PHP version with common extensions for Laravel.
  - **MySQL** – Latest version for managing your databases.
  - **Node.js (LTS)** – Installed via NVM.
  - **Composer** – A PHP dependency manager.
  - **Redis** – An in-memory store with PHP Redis extension.
  - **Supervisor** – For managing Laravel queue workers.

- **Generates SSH key for GitHub**: Set up GitHub SSH authentication on your server quickly.

## Prerequisites
- Ubuntu 24 or Debian-based systems.
- Sudo or root access.

## Installation Instructions

### 1. Save the Bash Script to Your Server

1. Create and edit the bash script file:
    ```bash
    nano setup_env.sh
    ```

2. Copy the content of the script into the file, then save and exit.

### 2. Give Execute Permissions

Make the script executable by running:
```bash
chmod +x setup_env.sh
```


### 3. Run the Script

Execute the script to install the packages:

```bash
./setup_env.sh
```


What’s Included
Nginx: A robust web server to host your Laravel applications.

PHP 8.3: Latest PHP version with essential extensions like:

php8.3-cli
php8.3-mysql
php8.3-curl
php8.3-xml
php8.3-mbstring
php8.3-zip
php8.3-bcmath
php8.3-gd
These extensions are perfect for Laravel development.

MySQL: The latest stable version of MySQL database server.

Node.js LTS: The latest long-term support version of Node.js installed using NVM, which is essential for running Laravel Mix.

Redis: Installed along with PHP Redis extension for session and cache handling in Laravel.

Supervisor: Ideal for managing Laravel queue workers.

Composer: The PHP package manager used to install Laravel and other PHP dependencies.

SSH Key Setup for GitHub
At the end of the script, an SSH key will be generated to streamline the connection between your server and GitHub.

You will be prompted to enter an email address (replace youremail@mailserver.com in the script with your actual email).
The script will display your public SSH key at the end. Copy it and add it to your GitHub SSH keys.
Optionally, the script will open GitHub settings in the browser if xdg-open is installed on your server.
Verifications
The script will display the versions of:

PHP
MySQL
Node.js
Redis
This helps you confirm that everything is installed correctly.

Ideal for Laravel Developers
This script is designed to make setting up a Laravel development environment on Ubuntu 24 as smooth as possible. It installs all the necessary components and packages required for Laravel projects, including Redis and Supervisor for managing queues and caching.

Notes
Make sure to replace the default email in the SSH key generation section with your own.
This script is optimized for Ubuntu 24 but should also work on other Debian-based distributions with minimal adjustments.
