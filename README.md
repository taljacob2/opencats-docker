# opencats-docker

This is a docker implementation for hosting [OpenCATS](https://github.com/opencats/OpenCATS) via docker-compose.

## Usage

Copy the [docker-compose.yaml](/docker-compose.yaml) file to your working directory, and run:

```sh
docker-compose up -d
```

- OpenCATS will serve at: http://localhost:8090
  - Follow through the [Installation Wizard](https://documentation.opencats.org/installation/run-the-installer), just press "test" and "next" all the way. Finally the Username and Passoword will be `admin` and `admin`.
- MySQL will serve at http://localhost:3307
- phpMyAdmin will serve at http://localhost:8080

## Development

First, git clone this repository.

### Build And Run The Image Locally

```sh
docker-compose -f docker-compose-dev.yaml up --build -d
```

- OpenCATS will serve at: http://localhost:8090
  - Follow through the [Installation Wizard](https://documentation.opencats.org/installation/run-the-installer), just press "test" and "next" all the way. Finally the Username and Passoword will be `admin` and `admin`.
- MySQL will serve at http://localhost:3307
- phpMyAdmin will serve at http://localhost:8080

### Build & Publish The Image On GitHub Repository

- Push to `master` branch to create `ghcr.io/taljacob2/opencats-docker:master`
- Push a git tag with a semantic tagging of `*.*.*` to create `ghcr.io/taljacob2/opencats-docker:*.*.*` and update `ghcr.io/taljacob2/opencats-docker:latest`
