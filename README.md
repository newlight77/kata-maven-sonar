# kata-maven-sonar

This is a demo multi-module project in java using powermock to unit test classes with static method calls. The code coverage is generated using jacoco you may then send metrics to SonarQube.

Jacoco and powermock don't work well together. In order to get coverage on classes using powermock, we must use jacoco in offline mode.

## Run

```sh
mvn clean install -Pcoverage
```

## Sonar

```sh
mvn sonar:sonar
```

# Docker

If you need an instance of SonarQube:

```sh
docker run -d --name sonarqube -p 9000:9000 sonarqube
docker run -d --name sonarqube -p 9000:9000 sonarqube:developer
docker run -d --name sonarqube -p 9000:9000 sonarqube:enterprise
```

## Reference

- [JaCoCo Offline Instrumentation can solve this problem](https://stackoverflow.com/questions/23983740/unable-to-get-jacoco-to-work-with-powermockito-using-offline-instrumentation)
- [Code Coverage with JaCoCo](https://github.com/powermock/powermock/wiki/Code-coverage-with-JaCoCo)