# Vehicle Rental Platform – Microservices System

## 📌 Project Overview

The Vehicle Rental Platform is a microservices-based system designed to provide a seamless experience for users looking to rent vehicles. The system allows users to browse available vehicles, view prices, and make reservations based on availability and location.

The solution follows the principles of **Clean Architecture**, ensuring:
- Business logic is independent of frameworks, databases, or delivery mechanisms.
- Each microservice is a standalone unit with clear, defined responsibilities.
- Dependencies point inward from infrastructure towards the core domain.

Users need an efficient and reliable way to:
- View available vehicles based on time, location, and preferences.
- Make a reservation for a chosen vehicle.
- Manage their reservations and personal data.

Administrators need the ability to:
- Add, edit, or remove vehicles from the system.
- Manage reservations made by users.

---

## 🧩 Microservices Overview

The system is composed of **three core microservices**, each responsible for a specific business domain:

### 1. 🚗 Vehicle Service
- **Responsibilities**:
  - Manages all vehicle-related data:
    - Add, edit, delete, search, and filter vehicles.
    - Tracks vehicle availability.
- **API**: Exposes a REST API for vehicle-related operations.
- **Database**: Owns its **own dedicated database**.

### 2. 📅 Booking Service
- **Responsibilities**:
  - Manages the entire booking lifecycle:
    - Create and cancel bookings.
    - Check vehicle availability for selected dates.
    - View booking history.
- **API**: Exposes a REST API for booking handling.
- **Database**: Has its **own booking-specific database**.

### 3. 👤 User Service
- **Responsibilities**:
  - Handles user management:
    - Registration and login.
    - Authentication and authorization.
    - Profile and reservation history access.
- **API**: Exposes a REST API for user operations.
- **Database**: Maintains a **separate user database**.

---

## 🧱 System Architecture Diagram

![MicroservicesScheme](https://github.com/user-attachments/assets/d1f6086b-0b7b-43db-9e99-3c0ca42f936b)

