# Costco Shopware POC Setup

This document provides a step-by-step guide to setting up a Shopware 6 instance using Dockware for the Costco proof of concept (POC). The setup involves creating a Docker environment, configuring it with Shopware, and ensuring it is accessible.

## Prerequisites

- **Docker**: Ensure Docker is installed and running on your system.
- **Docker Compose**: Required to manage multi-container Docker applications.

## Setup Instructions

### 1. Start Docker Daemon

Ensure that the Docker daemon is running. You can verify this by executing:

```sh
docker ps
```

This command should return a list of running containers, indicating that Docker is active.

### 2. Create `docker-compose.yml`

Create a `docker-compose.yml` file with the following content to configure the Shopware environment:

```yaml
services:
    shopware:
      image: dockware/dev:latest
      container_name: shopware
      ports:
         - "80:80"
         - "3306:3306"
         - "22:22"
         - "8888:8888"
         - "9999:9999"
      volumes:
         - "db_volume:/var/lib/mysql"
         - "shop_volume:/var/www/html"
      networks:
         - web
      environment:
         - XDEBUG_ENABLED=1

volumes:
  db_volume:
    driver: local
  shop_volume:
    driver: local

networks:
  web:
    external: false
```

### 3. Start Shopware Container

Run the following command to start the Shopware container:

```sh
docker-compose up -d
```

This command will pull the necessary Docker images and start the Shopware service in detached mode.

### 4. Verify Shopware Accessibility

After starting the container, verify that Shopware is accessible by executing:

```sh
curl -I http://localhost:80
```

You should receive an HTTP 200 OK response, indicating that the Shopware instance is running and accessible.

### 5. Restarting Dockware

If you need to restart the Dockware instance, you can do so with:

```sh
docker-compose restart
```

This command will restart the Shopware container without needing to rebuild the images.

## Notes

- The Shopware instance is configured to run on port 80. Ensure this port is available and not blocked by any firewall rules.
- The `XDEBUG_ENABLED` environment variable is set to `1` to facilitate debugging during development.

This setup provides a foundational environment for further customization and development tailored to Costco's branding and product requirements.
