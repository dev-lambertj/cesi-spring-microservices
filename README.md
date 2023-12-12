# Spring Boot Microservices with Gateway

# Description

This project consists in 2 microservices, each one dedicated to the management of one resource and exposing a RESTful
API for its resource:

- user, which manages basic users (username, firstName, lastName, createdAt, updatedAt)
- article, which manages basic blog articles (title, description).

It is also composed of a gateway which redirect requests to these microservices and receive requests on a single URI.

Finally, there is also a discovery service based on Eureka that discovers existing services which implement some
configuration related to this service.

# Requirements

You will need the following to start project:

* Docker (used 24.0.7 but any version should work).

# Starting the services

```shell
docker compose up -d
```

# Access the services

## Eureka

If you go to http://localhost:8761/ you will see the Eureka dashboard with the list of services registered.

## API usage

To use the APIs, use the following URIs:

* Users API: http://localhost:8088/api/users
* Articles API: http://localhost:8088/api/articles

# Resources

* https://www.javainuse.com/spring/cloud-gateway-eureka
* https://cloud.spring.io/spring-cloud-netflix/multi/multi__circuit_breaker_hystrix_clients.html
* https://cloud.spring.io/spring-cloud-gateway/reference/html/