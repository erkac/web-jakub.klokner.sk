# Docker Setup for jakub.klokner.sk

This directory contains Docker configuration to serve the website using nginx.

## Quick Start

### Using Docker Compose (Recommended)

```bash
cd docker
docker-compose up -d
```

The website will be available at: http://localhost:8080

### Using Docker directly

```bash
cd docker
docker build -t jakub-klokner-web .
docker run -d -p 8080:80 --name jakub-klokner-web jakub-klokner-web
```

## Commands

### Start the container
```bash
docker-compose up -d
```

### Stop the container
```bash
docker-compose down
```

### View logs
```bash
docker-compose logs -f
```

### Rebuild after changes
```bash
docker-compose up -d --build
```

## Configuration

- **Port**: The website runs on port 8080 by default. Change it in `docker-compose.yml` if needed.
- **Nginx config**: Customize nginx settings in `nginx.conf`
- **Website files**: Located in the `../web` directory

## Features

- Nginx Alpine for small image size
- Gzip compression enabled
- Security headers configured
- Static asset caching (1 year)
- Auto-restart unless stopped
