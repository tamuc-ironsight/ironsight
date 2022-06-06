# Ironsight Docker

## Description

All-in-one Ironsight files to setup Ironsight in Docker containers using Docker Compose.

## Installation / Usage

Clone this repository and navigate to that directory. You must set the the following environment variables (or create a .env file) to continue the setup:

```
IRONSIGHT_API_URL=https://IRONSIGHT_API_WEB_SERVER/ # External facing Ironsight API, users' browser will point to this
HARVESTER_URL=https://HAVESTER_INSTANCE/ # Harvester Web UI URL
MYSQL_ROOT_PASSWORD=changeme # (Optional, recommend using MYSQL_RANDOM_ROOT_PASSWORD instead)
MYSQL_RANDOM_ROOT_PASSWORD=yes
MYSQL_DATABASE=ironsight # This must match the PHP scripts. Safer to keep it the same
MYSQL_USER=ironsight
MYSQL_PASSWORD=ironsight
```

Once the environment variables are set, simply run `docker-compose up -d`. If you want a verbose log attached to your terminal (will be killed if you exit), then emit the `-d`.

## Roadmap

TBA

## License

TBA
