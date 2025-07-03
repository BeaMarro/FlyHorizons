# ✈️ FlyHorizons – Airline Booking System

FlyHorizons is an airline booking system I built as a solo project during **Semester 6 (Software Advanced)** by **Beatrice Marro** at **Fontys University of Applied Sciences**.

The system is built with **microservices**, runs on **Azure Kubernetes Service (AKS)**, and is designed to be fast, secure, and scalable.

---

## 📋 About the Project

This project simulates a real-world airline system. It lets users:
- Search for flights
- Select flight-related information, like luggage, seating and passengers
- Make complete bookings
- Handle (mock) payments
- Register, Login and Logout
- Admins can manage airports & flights
- Update account information, view collected personal data (GDPR) and delete the account

All features are split into different services that talk to each other using messages (RabbitMQ).

---

## 🧱 Microservices Overview

Here are the main services in this system:

| Service | What it Does | Link |
|--------|---------------|------|
| Booking Service | Books flights and reserves seats | [booking-service](https://github.com/beamarro/flyhorizons-booking-service) |
| Payment Service | Handles payments and transactions | [payment-service](https://github.com/beamarro/flyhorizons-payment-service) |
| Email Service | Sends emails and updates to users | [email-service](https://github.com/beamarro/flyhorizons-email-service) |
| Flight Service | Manages flight data and schedules | [flight-service](https://github.com/beamarro/flyhorizons-flight-service) |
| Airport Service | Manages airports | [airport-service](https://github.com/beamarro/flyhorizons-airport-service) |
| User Service | Manages user and admin accounts | [user-service](https://github.com/beamarro/flyhorizons-user-service) |
| API Gateway | Routes all requests and adds security | [api-gateway](https://github.com/beamarro/flyhorizons-api-gateway) |

---

## 🚀 How It’s Deployed

The app microservices run on **Azure Kubernetes Service (AKS)** and use:
- Docker containers for each service
- RabbitMQ for communication between services
- Kong API Gateway for security (rate limiting, authentication, etc.)
- Azure hosted MSSQL databases
- Kubernetes and Horizontal Pod Autoscaling to handle traffic

---

## ⚙️ Key Features

- Built with **Go** and **Gin** framework
- Uses **choreographed SAGA pattern** for handling distributed transactions
- Load tested to handle **3,500+ requests per second per pod**

---

## 🧰 Tech Stack

| Area        | Tools & Technologies |
|-------------|----------------------|
| Backend     | Go (Gin), RabbitMQ   |
| Frontend    | React, React Bootstrap |
| API Gateway | Kong                 |
| DevOps      | Docker, Kubernetes, Microsoft Azure |
| Database    | MSSQL, Microsoft Azure           |

---

## 🖼️ System Architecture

A system architecture diagram, as a C3 diagram, can be found below:

```markdown
![C3 Diagram](./C3%20Diagram.drawio.png)
```

## 📄 License
This project is shared for educational and portfolio purposes only.
**Commercial use, redistribution, or modification is not allowed without explicit written permission.**
All rights reserved © 2025 Beatrice Marro.

## 👤 Author
Beatrice Marro
GitHub: https://github.com/beamarro
