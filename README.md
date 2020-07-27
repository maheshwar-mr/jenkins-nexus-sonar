# Jenkins and Nexus using docker-compose

## Volumes

Before starting up the containers, the volumes for respective tools need to be created

```bash
docker volume create --name jenkins-volume
docker volume create --name nexus-data
```

## Running the containers

To start both Jenkins and Nexus containers, use the following command

```bash
docker-compose up --build -d
```

Jenkins and Nexus can be accessed on the host ports 8080 and 8081 respectively
