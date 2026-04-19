# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

# Prerequisites

Make sure the following are installed:

1- Docker

2- Docker Compose

Verify installation:

1- docker --version

2- docker compose version

<img width="512" height="116" alt="image" src="https://github.com/user-attachments/assets/7f9f7008-518b-45c5-9814-a1b7998a467d" />

### Adding Docker Configuration Files

To containerize the application, the following files must be created:

---

### 1. Dockerfile (for each service)

Each service must conatain a `Dockerfile` 
(`user-service`, `product-service`,c`order-service`, `gateway-service`)


### 2. docker-compose.yml

A `docker-compose.yml` file is required in the root directory to orchestrate all services.

---

## Build and run containers
```
docker-compose up --build
```
This will:

1- Build Docker images for all services

2- Start all containers

3- Create a shared network

## Services and Endpoints

### Access the Individual Services

### 1- User Service 
#### URL: http://localhost:3000/users

<img width="526" height="247" alt="image" src="https://github.com/user-attachments/assets/53e2b47e-1e60-4c45-9f49-1d31cc0626c7" />


### 2- Product Service 
#### URL:http://localhost:3001/products

<img width="658" height="235" alt="image" src="https://github.com/user-attachments/assets/87742e87-9ee7-4457-9038-683a1e49b26c" />


### 3- Order Service
#### URL: http://localhost:3002/orders

  a- Initally Orders are empty
<img width="530" height="178" alt="image" src="https://github.com/user-attachments/assets/fed139f4-bc04-4469-8e80-5f368bbcaa87" />


  b- Adding data through postman
<img width="553" height="465" alt="image" src="https://github.com/user-attachments/assets/63b18bee-c417-4ada-ab15-69d8f0b6a681" />

  c- With data
<img width="365" height="108" alt="image" src="https://github.com/user-attachments/assets/4a50a4ee-061d-422f-aaa1-a7dfec74f298" />

### Access using Gateway Service

### 1- User Service 
#### URL: http://localhost:3003/api/users

<img width="541" height="160" alt="image" src="https://github.com/user-attachments/assets/a538d583-78dd-4bfb-92eb-980df5756ea8" />


### 2- Product Service 
#### URL:http://localhost:3003/api/products

<img width="638" height="137" alt="image" src="https://github.com/user-attachments/assets/ce3cd4b8-8b31-4165-822d-ed21634093d2" />



### 3- Order Service
#### URL: http://localhost:3003/api/orders

<img width="433" height="123" alt="image" src="https://github.com/user-attachments/assets/bea06dda-711c-4c06-9c55-f7d2b923b210" />

---
