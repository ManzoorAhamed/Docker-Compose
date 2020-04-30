# Docker-Compose
Docker Compose to setup WordPress MySql phpMyAdmin and cAdvisor on the go.

With this project you can quickly run the following:

- WordPress
- phpMyAdmin
- MySql
- cAdvisor

Contents:

- Requirements
- Installation
- Usage

## Requirements:

- Docker + Docker Compose
- Make sure you have the latest version of Docker and Docker Compose installed on your machine.

## Installation

Open the terminal and `cd` to the folder in which `docker-compose.yml` is saved and run:

```
docker-compose up
```

This command will download the all the necessary images for the container to run. In case the images are already in the system then it wont download. 

The compose file make sure the container launch in an order, So the connectivity from the web to DB container get established properly.

## Usage

### Starting the containers

You can start the container with the up command in daemon mode or by using the start command

```
docker-compose start
```

### Stopping the containers

```
docker-compose stop
```

### Removing the containers

To stop and remove all the containers use the down command

```
docker-compose down
```

Use -v if you need to remove the database volume which is used to persist the database:

```
docker-compose down -v
```

## phpMyAdmin:

You can also access phpMyAdmin after starting the containers.

The default username is `root`, and the password is the same as supplied in the compose file.

## cAdvisor

- cAdvisor stands for `Container Advisor`.
- As it is evident from the name it provides resource usage, performance characteristics & related information about the containers running on the cloud.
- It is an open-source tool & runs as a daemon process in the background collecting, processing & aggregating useful DevOps information.
- The tool has native support for Docker & enables us to track historical resource usage. This helps in understanding the resource consumption, memory footprint of the code running on the servers.

## Accessing the Containers
- WordPress	`localhost:8080`
- phpMyAdmin	`localhost:8000`
- cAdvisor	`localhost:8081`
