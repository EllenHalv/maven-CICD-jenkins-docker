# maven-test

## Description
This is a test application for creating a CI/CD pipeline for a maven project using Jenkins and Docker.

## Prerequisites
- Docker
- Jenkins
- Maven
- Java
- Git

## How to use
For Docker-compose:
```bash
docker-compose -f docker/docker-compose.yaml up -d
```

1. go to http://localhost:8080/ and login

2. go to http://localhost:1025/ to see that the mailhog is running

3. configure Jenkins system settings to use the mailhog

4. configure a job to notify a random email address

5. run the job

6. go to http://localhost:1025/ to see that the mailhog received the email
