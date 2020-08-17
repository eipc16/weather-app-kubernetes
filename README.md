# Distributed Weather App

Simple weather app application built with Quarkus and Kubernetes that uses OpenWeather API
as a data source and Infinispan for distributed cache.

## Build

| Job               | Status        |
| ----------------- | ------------- |
| master build      | [![Build Status](https://travis-ci.org/eipc16/weather-app-kubernetes.svg?branch=master)](https://travis-ci.org/eipc16/weather-app-kubernetes)         |

## Progress
### Steps
- [X] Travis setup
- [X] Quarkus setup
- [ ] React setup
- [ ] Serve React frontend from Quarkus
- [ ] Implement API using OpenWeatherAPI
- [ ] Basic frontend
- [ ] Kubernetes setup
- [ ] Implement distributed cache with Infinispan
- [ ] First release

### Future work
- [ ] Deploy to cloud
- [ ] Create React Native app for mobile devices
- [ ] Configure Swagger

## API Documentation

    TODO: Document the API

## The application

    TODO: Add screenshots

## Usage
### Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```
./mvnw quarkus:dev
```

### Packaging and running the application

The application can be packaged using `./mvnw package`.
It produces the `weather-app-kubernetes-1.0.0-SNAPSHOT-runner.jar` file in the `/target` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/lib` directory.

The application is now runnable using `java -jar target/weather-app-kubernetes-1.0.0-SNAPSHOT-runner.jar`.

### Creating a native executable

You can create a native executable using: `./mvnw package -Pnative`.

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: `./mvnw package -Pnative -Dquarkus.native.container-build=true`.

You can then execute your native executable with: `./target/weather-app-kubernetes-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/building-native-image.