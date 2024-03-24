# Docker Project Description

## Overview:
This Docker project aims to set up a robust environment for hosting web services with Nginx, Let's Encrypt SSL certificates, and OpenVAS vulnerability scanning.

## Project Structure:

my_docker_project/
│
├── conf/
│   ├── nginx.conf
│   └── nginx_ssl.conf
│
└── data/
    ├── letsencrypt/
    └── letsencrypt-www/


## Project Structure:

- **conf/**: Contains configuration files for Nginx servers.
  - `nginx.conf`: Configuration for the HTTP Nginx server.
  - `nginx_ssl.conf`: Configuration for the HTTPS Nginx server.

- **data/**: Directory for storing Let's Encrypt SSL certificates and related data.
  - `letsencrypt/`: Stores Let's Encrypt SSL certificates.
  - `letsencrypt-www/`: Directory for Let's Encrypt related data.

## Docker Services:

- **nginx**: Nginx server for handling HTTP requests.
- **nginx_ssl**: Nginx server configured for HTTPS with Let's Encrypt certificates.
- **letsencrypt**: Service for obtaining and renewing Let's Encrypt SSL certificates.
- **openvas**: OpenVAS vulnerability scanner.
- **cron**: Cron job for scheduling tasks related to OpenVAS updates.

## Usage:

1. Ensure Docker and Docker Compose are installed.
2. Clone or create the project directory.
3. Place appropriate configuration files in the `conf/` directory.
4. Run `docker-compose up -d` to start the services defined in `docker-compose.yml`.

## Notes:

- Replace `example.com` with your actual domain name in configuration files.
- Ensure proper permissions for directories storing SSL certificates.
