# Unlimited testing environments with Codefresh and Kubernetes


This is an example Java application that uses Spring Boot 2, Maven and Docker.
It is compiled using Codefresh.

## Instructions

To compile (also runs unit tests)

```
mvn package
```

## Create a multi-stage docker image

To compile and package using Docker multi-stage builds

```bash
docker build . -t my-spring-boot-sample
```

## To run the webapp manually

```
docker run -p 8080:8080 my-spring-boot-sample
```

....and navigate your browser to  http://localhost:8080/

The Dockerfile also has a healthcheck

## To run integration tests

```
docker run -p 8080:8080 my-spring-boot-sample
mvn verify
```

## To use this project in Codefresh 


There is also a [codefresh.yaml](codefresh.yaml) for easy usage with the [Codefresh](codefresh.io) CI/CD platform.


More details can be found in [Codefresh documentation](https://codefresh.io/docs/docs/ci-cd-guides/unlimited-testing-environments/)


Enjoy!
