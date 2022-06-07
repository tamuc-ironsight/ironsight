# Ironsight Docker

## Description

All-in-one Ironsight files to setup Ironsight in Docker containers using Docker Compose.

## Installation / Usage

Clone this repository and navigate to that directory. You must set the the following environment variables (or create a .env file) to continue the setup:

```bash
IRONSIGHT_API_URL=https://IRONSIGHT_API_WEB_SERVER/ # External facing Ironsight API, users' browser will point to this
HARVESTER_URL=https://HAVESTER_INSTANCE/ # Harvester Web UI URL

MYSQL_ROOT_PASSWORD=changeme # (Optional, recommend using MYSQL_RANDOM_ROOT_PASSWORD instead)
MYSQL_RANDOM_ROOT_PASSWORD=yes
MYSQL_DATABASE=ironsight
MYSQL_USER=ironsight
MYSQL_PASSWORD=ironsight
MYSQL_RANDOM_ROOT_PASSWORD=yes

HARVESTER_API_TOKEN=token-#### # Harvester API generated token

ELASTIC_FLEET_URL=https://ELASTIC_FLEET_URL # Ommit slash, bug needs fixing
ELASTIC_FLEET_API_TOKEN=TOKEN_HERE
ELASTIC_VERSION=8.1.2

ELASTICSEARCH_URL=https://ELASTIC_URL/
ELASTICSEARCH_API_TOKEN= # Elasticsearch token with reporting access

IRONSIGHT_API_TOKEN=test_token # Non-functional for now
```

Once the environment variables are set, simply run `docker-compose up --build -d`. If you want a verbose log attached to your terminal (will be killed if you exit), then omit the `-d`.

## Roadmap

### High Priority

- Class lists / multi-student deployment

- Multi-VM lab support

- Guacamole integration

- SecurityOnion / SIEM integration

### Other

- VLAN management

- Container support

- Ansible integration

- More flexible cloud-init customization from frontend

## License

[MIT License](https://opensource.org/licenses/MIT)
