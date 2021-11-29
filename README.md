# Docker Datacenter

Docker configurations for various Big Data applications

## Installation

Please install [Docker and Docker Compose](https://www.docker.com/) first.

```bash
# Building Base Images
docker-compose -f docker-compose-build.yml up -d --build
docker-compose -f docker-compose-build.yml down

# Create default containers network
docker network create -d bridge data-center
```

## Usage

```bash
# Create Hadoop Container
docker-compose -f docker-compose-hadoop.yml up -d

# Create HBase Container
docker-compose -f docker-compose-hbase.yml up -d

# Stop Container
docker-compose -f docker-compose-hadoop.yml stop
docker-compose -f docker-compose-hbase.yml stop

# Drop/Delete Container
docker-compose -f docker-compose-hadoop.yml down
docker-compose -f docker-compose-hbase.yml down
```

## License
[MIT](https://choosealicense.com/licenses/mit/)