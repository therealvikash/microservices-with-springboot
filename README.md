# Microservice Architecture with Spring Boot

This repository demonstrates a microservice architecture implemented with Spring Boot, following best practices for building scalable, distributed systems. It includes components such as an API Gateway, Configuration Server, Service Registry, Circuit Breaker (Hystrix), and two interacting microservices

## Microservice with Spring Boot
|Field|    Value   |
|-----|-------------|
|Title|Microservice |
|Author(s)|Bikashs Kumar Yadav|

## Features
1. API Gateway: A centralized entry point for the microservices.
2. Service Registry (Eureka): For registering and discovering microservices.
3. Configuration Server: Centralized configuration management for the microservices.
4. Hystrix: Circuit breaker for handling fault tolerance and resilience in microservices.
5. Two Services: Services that communicate with each other, demonstrating inter-service communication.

## Architecture
The system consists of the following components:

1. API Gateway: Acts as a proxy and routes requests to the respective microservices.
2. Config Server: Manages the configuration for all microservices.
3. Service Registry (Eureka): Registers microservices for discovery and load balancing.
4. Hystrix: Provides circuit breaker functionality to prevent cascading failures.
5. employee-service: A sample microservice.
6. department-service: Another sample microservice that interacts with employee-service.

## Project Structure
├── api-gateway/<br>
├── config-server/<br>
├── department-service/<br>
├── employee-service/<br>
├── hystrix-dashboard/<br>
├── service-registry/<br>
├── .gitignore/<br>
└── README.md

## Technologies Used
1. Java 17
2. Spring Boot
3. Spring Cloud Config
4. Netflix Eureka (Service Registry)
5. Netflix Hystrix (Circuit Breaker)
6. Spring Cloud Gateway (API Gateway)
7. Gradle(Build Tool)

## Prerequisites
1. Java 17: Make sure you have Java 17 installed.
2. Gradle: Ensure you have Gradle installed to build and manage dependencies.
3. Git: Clone this repository using Git.

## Setup & Running
1. cd <filename> Navigate to each project
2. ./gradlew bootRun

## Hystrixx Dashboard
You can view the Hystrix dashboard to monitor circuit breaker status:
1. [Hystrix Dashboard](http://localhost:9295/hystrix)

## Eureka Service Registry
You can view the Service Registry dashboard to monitor the services up and runnning at:
1. [Service Registry](http://localhost:8761)

## Usage
Once all services are up and running:

1. API Gateway: Make HTTP requests to the API Gateway, which will route them to the corresponding microservice.
  * Example:
    * [department-service](http://localhost:8060/department/*)
    * [employee-service](http://localhost:8060/employee/*)
2. Service Discovery: Services will automatically register with Eureka and be discoverable via the service registry.
3. Fault Tolerance: Hystrix will ensure resilience by applying circuit breakers for remote calls between services.

## Configuration Management:

config-repo/<br>
├── application.yml<br>
├── department-service.yml<br>
└── employee-service.yml<br>
└── hystrix-dashboard.yml

## Circuit Breaker (Hystrix)
Hystrix is integrated to provide fault tolerance. If a service is down or taking too long to respond, Hystrix opens the circuit to prevent further requests from being sent to the service.

You can monitor the status of circuits and view metrics on the Hystrix Dashboard.

## Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.

## License
This project is not licensed under any specific open-source license. You are free to use, modify, and distribute the code as per the terms you see fit, but it is recommended to clarify terms of use with the repository owner before significant reuse.

## 
This README provides an overview of the microservices project, how to set it up, and details about its components. You can customize it further based on your specific implementation.
