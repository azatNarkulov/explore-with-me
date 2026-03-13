# Explore With Me

Backend service for sharing and discovering events.
Users can publish events, explore upcoming activities and join events created by others.

The project demonstrates building a RESTful backend application using Java and Spring Boot with a microservice-based architecture.

---

## Features

* Create and manage events
* Browse and search events with filtering and sorting
* Send participation requests for events
* Event moderation by administrators
* Event categories and user management
* Collection of statistics about requests and views

---

## Architecture

The application follows a **microservice architecture** and consists of two main services:

**Main service**

* handles users, events, categories and participation requests

**Statistics service**

* collects and aggregates endpoint hit statistics

Services communicate via REST API and can be run using Docker.

---

## Tech Stack

**Backend**

* Java
* Spring Boot
* REST API
* Maven

**Persistence**

* PostgreSQL / H2
* JPA / Hibernate

**Other**

* Docker
* Lombok
* MapStruct
* Postman (API testing)

---

## API

The project exposes REST endpoints for three types of access:

* **Public API** — view events and categories
* **Private API** — manage user events and participation requests
* **Admin API** — moderation and management of platform data

API specifications are available in:

* `ewm-main-service-spec.json`
* `ewm-stats-service-spec.json`

---

## Running the project

### Requirements

* Java 11+
* Maven
* Docker (optional)

### Run with Docker

```bash
docker-compose up
```

### Run locally

```bash
mvn clean package
mvn spring-boot:run
```

---

## Project Structure

```
main-service     — core business logic and API
stats-service    — statistics collection service
postman          — API testing collection
docker-compose.yml
```

---

## Purpose of the project

This project was developed as a project to practice:

* backend development with Spring Boot
* REST API design
* database interaction with JPA/Hibernate
* microservice architecture
* Docker-based deployment
