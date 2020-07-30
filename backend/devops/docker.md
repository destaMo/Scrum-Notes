# DevOps - docker / docker compose / docker for development

technology lead: Bartlomiej Danek

## What is Docker?

Docker is an open source tool for running isolated containers on Linux making the deployment of apps inside containers faster. Docker creates portable, self-sufficient containers from any application.

The same container that the developer builds and tests on his PC can run in production, on VMs, in the cloud and a lot more places.

## Why should I use Docker?

- consistent development environment for entire team
- you need only Docker to develop
- it helps to minimize the differecens between local and production environments
- environment is isolated from dev. OS and other tools

## Learning

### Online

- [Docker Docs](https://docs.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/compose-file/)
- [Devhints](https://devhints.io/docker)
- [Docker Playground](https://labs.play-with-docker.com)

### Selleo Books

- [Deployment with Docker](https://docs.zoho.eu/ws/pulse/file/3szsc1d6e4e923f554fa4b0a57a58a445c96c)
- [DevOps for Networking](https://docs.zoho.eu/ws/pulse/file/3szsc854d03dc0bb3403a8d7436ddea2079ad)
- [Getting Started with Kubernetes](https://docs.zoho.eu/ws/pulse/file/3szsce8675e16a21d4a79a00a5645e0f34b3c)

## Requirements

Prerequisites:

- Docker engine: Engine: 18.06 or newer

### Independent 1 - Independent 3

You need to:

- know how Linux system works
- have a basic knowledge about Linux administration e.g.
  - shell
  - ENV variables
  - BASH scripting
- know how to work/administrate databases (SQL/NoSQL) or linux services
- have a basic know-how about network administration and Nginx configuration

#### Exercise 1

- [ ] Prepare a *Dockerfile* which will run [sample script](docker/exercises/sample_script) :small_blue_diamond:

#### Exercise 2

- [ ] Prepare a *Dockerfile* which will install a working (nodejs, npm, yarn) environment for a nodejs application in version defined in `NODE_VERSION` environment variable. :small_blue_diamond:

> **Note:**
> Please **DO NOT USE** containers delivered by community.

#### Exercise 3

- [ ] Preapre a *Dockerfile* which will setup and run a Rails app (use local instances of a database or cache engine). :small_blue_diamond:

> **Note:**
> Please **DO NOT USE** containers delivered by community.

#### Exercise 4

- [ ] Prepare a *Dockerfile* for one of 3rd part services (database, cache storage, search engine etc.) what you use in one of your apps.
Replace the service by a service served by Docker. :small_blue_diamond:

#### Exercise 5

- [ ] Prepare a working *docker-compose.yml* file which will run [advanced rails application](docker/exercises/sample_app) :small_orange_diamond: :

* Rails 5.2 application with Ruby 2.5.1
* PostgreSQL 10.5
* Redis 4.0
* Memcached 1.5

The app is using:

* Websockets
* Sidekiq as a background worker
* Nginx on the top
* Memcached as a cache storage

#### Exercise 6

- [ ] Provide a working soultion with Docker Compose for the app :small_orange_diamond:

> **Note:**
> Feel free to use containers delivered by community.
