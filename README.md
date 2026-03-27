# Docker Configs

Docker Compose configurations for self-hosted services running on Ubuntu Server 24.04, managed via Portainer with Caddy as reverse proxy and Cloudflared as tunnel.

## Prerequisites

### Create the proxy network

Before deploying any stack, create the shared Docker network:

```bash
docker network create proxy-network
```

All services use this external network to communicate with the Caddy reverse proxy.

## Services

| Service     | Port | Description              |
| ----------- | ---- | ------------------------ |
| Portainer   | 9443 | Docker management UI     |
| Immich      | 2283 | Photo & video management |
| Uptime Kuma | -    | Uptime monitoring        |
| Netdata     | -    | Server monitoring        |
| Linkwarden  | 3003 | Bookmark manager         |

## Data Storage

- Docker service data: `/mnt/nas/data/docker/{service_name}`
- Media files: `/mnt/nas/data/{images,videos,documents,music,photos}`
