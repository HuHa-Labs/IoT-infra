# IoT Microservices

## Aims and purposes
This project is created for demo purposes, demonstrating my learning 
progress in constructing microservices, understanding several communication 
protocols and utilising a variety of programming tools.

This project aims to simulate an IoT system, which supports reading, 
processing, and visualising data from Iot devices. Specifically, an IoT 
devices will send data to the server. Then, the data will be 
processed and stored into a database. Finally, the processed data can be 
queried and visualised on charts for monitoring purposes.

## Out-of-scope
This project does not aim to use a real IoT devices (though that is a 
fascinating learning opportunity). So, no data in this project is real, but 
rather fabricated from simulated IoT devices in Docker.

## Tech-stack and Architecture
### Tech-stack:
#### Infrastructure:
- Docker: setups dev environment and  containerises microservices. 
  - One of the huge 
    advantages brought about Docker is that it standardises the process of 
    running any services for development. A container
    comes in package with necessary software setup and run-time environment,
    reducing the hassle of building everything from scratch. 
  - Another advantage is that it offers a textual, miscommunication-free deployment 
    instruction. A deployer can easily set up a deployment container using the 
    image provided by developers.
  - For the project, docker is used for setting up complex development 
    services such as simulated IoT devices and database, and isolating the 
    microservices in the deployment.

- Kubernetes (k8s): manages several containers on deployment. (TBD)
- Kafka: acts as (TBD). It receives data from IoT devices using MQTT 
  protocol, the process and stream data to the server

#### Server
The server is the heart of the system, whose missions are reading, 
processing, storing, and providing data for visualisation.

The server will be written in C# (TBD, more about the framework).

#### Database
The database used for this project is PostgreSQL, a powerful relational 
database. 

**PostgreSQL vs InfluxDB** (TBD)


#### Frontend
For visualisation, Vue.js with Typescript is used to build a dashboard. The 
frontend will communicate with the server using REST API.

**Vue.js vs Grafana dashboard** (TBD)