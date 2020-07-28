# Jenkins, Nexus and Sonar as docker containers

## Running the containers

Use the following commands from the **jenkins-nexus-sonar** directory to start up Jenkins, Sonar and Nexus as docker containers

```bash
docker-compose up -d
docker-compose up -f sonar/docker-compose.yml -d
```

Jenkins, Nexus and Sonar can now be accessed on the host ports 8080, 8081 and 9000 respectively
