# SonarQube

This is my local SonarQube setup using Docker Compose.
State is persisted in a PostgreSQL database.

## Usage

Use [docker-compose](https://github.com/docker/compose) to start the containers:

```
$ docker-compose up -d
```

After upgrading or installing a plugin,
restart SonarQube:

```
$ docker-compose restart sonarqube
```

Run the following Maven command to analyse a project:

```
$ mvn sonar:sonar \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.jdbc.url=jdbc:postgresql://localhost/sonar
```
