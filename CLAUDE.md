all data are in /mnt/nas/data/{images,videos,documents,music,photos,}
when you create a docker compose file

- keep configuration as simple as possible
- verify on internet the latest configuration
- inside docker-compose.yml create envs block to share between services, create .env.example and .env to store variables
