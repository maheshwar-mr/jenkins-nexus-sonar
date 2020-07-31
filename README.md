# Jenkins, Nexus and Sonarqube as docker containers

## Running the containers

Use the following commands from the **jenkins-nexus-sonar** directory to start up Jenkins, Sonar and Nexus as docker containers

```bash
docker-compose up -d
docker-compose -f sonar/docker-compose.yml up -d
```

Jenkins, Nexus and Sonarqube can now be accessed on the host IP at ports 8080, 8081 and 9000 respectively

## Jenkins Initial Admin Password

Use the following command to get the default Jenkins password

```bash
docker exec -it jenkins-nexus-sonar_jenkins_1 cat /var/jenkins_home/secrets/initialAdminPassword
```

Copy this password and paste it when asked for on http://YOUR_HOST_IP:8080 to continue to install plugins and create a user

## Nexus Initial Credentials

Use the following command to get the default Nexus password

```bash
docker exec -it jenkins-nexus-sonar_nexus_1 cat /nexus-data/admin.password
```

Use **admin** as the username and the **result of the above command** as the password to continue to the Setup Wizard

## Sonarqube Initial Credentials

username: **admin**

password: **bitnami**
