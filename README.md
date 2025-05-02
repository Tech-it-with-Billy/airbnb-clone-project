# Airbnb Clone Project
### Project Overview

The AirBnB Clone backend replicates the core functionality of the AirBnB platform. It provides a scalable and secure foundation for managing users, property listings, bookings, payments, and reviews. This backend supports RESTful and GraphQL APIs to ensure flexible and efficient communication with the frontend.

### Project Goals

User Management: Register, authenticate, and manage user profiles securely.

Property Listings: Allow hosts to create, update, and manage rental properties.

Booking System: Enable users to book properties and manage reservations.

Payment Processing: Integrate payment workflows for bookings.

Review System: Support posting and managing reviews for properties.

Performance: Optimize data handling through indexing and caching.

### Tech Stack

Backend Framework: Django

API Development: Django REST Framework, GraphQL

Database: PostgreSQL

Asynchronous Tasks: Celery

Caching & Session Management: Redis

Containerization: Docker

CI/CD: GitHub Actions (or any CI tool of choice)

### Team Roles

Backend Developer: Builds and maintains API endpoints and core backend logic.

Database Administrator: Designs and optimizes the PostgreSQL database for performance and reliability.

DevOps Engineer: Manages deployment, infrastructure, and CI/CD pipelines.

QA Engineer: Tests API functionality and ensures bug-free, reliable backend performance.

### Here’s a brief explanation of each technology mentioned in your project overview:

## Technology Stack

* **Django**: A web framework for building and structuring the backend and RESTful APIs.
* **Django REST Framework (DRF)**: Extends Django to create and manage RESTful APIs efficiently.
* **PostgreSQL**: A robust relational database for storing and querying structured data.
* **GraphQL**: Provides a flexible way to query and manipulate data via a single endpoint.
* **Celery**: Handles background tasks like sending emails or processing payments asynchronously.
* **Redis**: Used for caching and managing session data to improve performance.
* **Docker**: Containerizes the application for consistent development and deployment environments.
* **CI/CD Pipelines**: Automate testing and deployment to ensure smooth integration of code changes.

Sure! Here's a shortened version with concise fields and relationships:

---

## Database Design

### **User**

**Fields:** `id`, `username`, `email`, `role`, `date_joined`
**Relations:** Can own properties, make bookings, and leave reviews.

### **Property**

**Fields:** `id`, `title`, `description`, `location`, `price_per_night`
**Relations:** Belongs to a user; has many bookings and reviews.

### **Booking**

**Fields:** `id`, `user`, `property`, `check_in`, `check_out`
**Relations:** Made by a user for a property; linked to a payment.

### **Payment**

**Fields:** `id`, `booking`, `amount`, `date`, `status`
**Relations:** Tied to one booking.

### **Review**

**Fields:** `id`, `user`, `property`, `rating`, `comment`
**Relations:** Written by a user about a property.
