# Current configuration

We are using ubuntu server 24.04
We are using portainer as docker compose manager
We are using caddy as reverse proxy
We are using cloudflared as tunnel

## Instruction when installing new services

- keep configuration as simple as possible
- verify on internet the latest configuration
- inside docker-compose.yml create envs block to share between services, create .env.example and .env to store variables

# Data storage

user data should be stored in /mnt/nas/data/{images,videos,documents,music,photos,games}
docker data services should be store in /mnt/nas/docker/{service_name}
