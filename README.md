# Dockerizing Spring Boot Application &amp; Kafka Broker

## Introduction
The purpose of the repository is to showcase how to dockerize a Spring Boot application as well as a Kafka Broker (along with Zookeeper) on either a Single Host Server or on a Swarm Cluster.

We know dockerization can be used for:
- Development environment
- Automated testing environment
- Single host deployment
- Swarm cluster deployment

On a Swarm cluster, the Swarm mode features:
- Scaling
- Load balancing
- Decentralized design
- Multi-host networking
- Declarative service model
- Service discovery
- Rolling updates
- etc.

The Spring Boot application uses Spring Cloud Stream to communicate (publish/receive messages) with Kafka message broker. The application simulates a compute engine to perform simple calculating tasks generated by REST 'send' request, and return the result to the user by REST 'receive' request. It uses Kafka topics to store requests and responses.

![The Design Diagram](https://github.com/MikeQin/dockerizing-springboot-kafka/raw/master/images/Design.png)

## Preparation: Docker Images
To facilitate the demostration of dockerization, I created two docker images:
- [Spring Boot Application Docker Image](https://hub.docker.com/r/michaeldqin/springboot-kafka/)
- [Kafka Docker Image](https://hub.docker.com/r/michaeldqin/kafka/)

![Topology](https://github.com/MikeQin/dockerizing-springboot-kafka/raw/master/images/DockerizingAppKafka.png)

Both docker images are used to create multiple docker containers, which are managed through docker-compose. The docker-compose prescribes the docker stack, services, networks, and deployment, etc.

## Running the Spring Boot Application and Kafka Server on a Single Host Server

### Docker-Compose-Single-Host File

## Running the Spring Boot Application and Kafka Server on a Swarm Cluster

### Docker-Compose-Swarm-Cluster File

### Testing Load Balancing

### Testing Scaling

