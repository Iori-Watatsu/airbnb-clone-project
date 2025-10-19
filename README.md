## Airbnb Clone Project — StayBackend

Welcome to the Airbnb Clone Project, a full-stack application inspired by Airbnb’s core features.
This project focuses on backend architecture, database design, API development, and security implementation — building a real-world booking system for users, hosts, and travelers.

### Project Goals

The main goal of this project is to simulate how large-scale web applications like Airbnb are built and maintained.
Through this experience, we aim to:

- Master backend architecture and RESTful API development.

- Design a scalable relational database structure using MySQL or PostgreSQL.

- Apply security best practices for user authentication and data protection.

- Automate the deployment process using CI/CD pipelines.

- Collaborate effectively using GitHub and version control workflows.\

### Team Roles
| Role                             | Description                                                                                                          |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Backend Developer**            | Responsible for implementing the business logic, building RESTful APIs, and integrating database models with Django. |
| **Database Administrator (DBA)** | Designs and manages the database schema, ensures data consistency, and optimizes query performance.                  |
| **Frontend Developer**           | (If applicable) Works on the user interface, integrating backend APIs and ensuring a smooth user experience.         |
| **DevOps Engineer**              | Handles CI/CD pipelines, Docker configurations, and server deployment to ensure a stable environment.                |
| **Project Manager**              | Coordinates team progress, assigns tasks, and ensures milestones are achieved on time.                               |
| **QA Engineer**                  | Tests endpoints, verifies data integrity, and ensures all features meet project requirements.                        |

### Technology Stack
| Technology             | Purpose                                                                                                |
| ---------------------- | ------------------------------------------------------------------------------------------------------ |
| **Django**             | The core backend framework used to build scalable and maintainable RESTful APIs.                       |
| **MySQL / PostgreSQL** | The relational database systems that store all application data — from users to bookings and payments. |
| **GraphQL**            | Provides an efficient query interface for fetching complex, related data structures.                   |
| **Docker**             | Used to containerize the application for consistent environments during development and deployment.    |
| **GitHub Actions**     | Powers the CI/CD pipeline for automating testing and deployment.                                       |
| **Nginx / Gunicorn**   | Handles reverse proxying and web server configurations for production.                                 |

### Database Design

Here’s a high-level overview of the main entities and their relationships:

| Entity         | Key Fields                                                            | Description                                                     |
| -------------- | --------------------------------------------------------------------- | --------------------------------------------------------------- |
| **Users**      | `id`, `name`, `email`, `password_hash`, `role`                        | Represents hosts and guests who interact with the system.       |
| **Properties** | `id`, `owner_id`, `title`, `location`, `price`, `availability_status` | Each property is owned by a user and can be booked by others.   |
| **Bookings**   | `id`, `user_id`, `property_id`, `check_in`, `check_out`, `status`     | Tracks reservations made by users for specific properties.      |
| **Reviews**    | `id`, `user_id`, `property_id`, `rating`, `comment`                   | Allows guests to rate and review properties they’ve stayed at.  |
| **Payments**   | `id`, `booking_id`, `amount`, `payment_method`, `status`              | Stores information about transactions and payment verification. |

**Relationships:**

- A User can own multiple Properties.

- A Property can have multiple Bookings and Reviews.

- Each Booking is linked to a Payment record.

- A User can also be both a host and a guest.

### Future Breakdown

| Feature                 | Description                                                                          |
| ----------------------- | ------------------------------------------------------------------------------------ |
| **User Management**     | Handles registration, authentication (JWT or OAuth), and user profile management.    |
| **Property Management** | Allows hosts to list properties, set availability, and manage pricing.               |
| **Booking System**      | Enables users to search for properties, make reservations, and view booking history. |
| **Reviews and Ratings** | Lets guests leave feedback and rate their stay experiences.                          |
| **Payment Integration** | Supports secure payment methods and transaction tracking for bookings.               |
| **Admin Dashboard**     | Provides admins with tools for managing users, listings, and reports.                |

Each feature directly contributes to replicating Airbnb’s key functions in a simplified, educational way.

### API Security

Security is a cornerstone of this project. Key measure include:

| Measure                                       | Purpose                                                                       |
| --------------------------------------------- | ----------------------------------------------------------------------------- |
| **Authentication (JWT)**                      | Ensures only verified users can access or modify protected resources.         |
| **Authorization (Role-based Access Control)** | Restricts certain actions to admins or property owners only.                  |
| **Input Validation**                          | Prevents SQL injections and data corruption by sanitizing user inputs.        |
| **Rate Limiting**                             | Protects APIs from brute-force or DDoS attacks by limiting repeated requests. |
| **Data Encryption (HTTPS/TLS)**               | Ensures all data transfers are securely encrypted between client and server.  |

### CI/CD Pipeline

Continous Intergration/Continous Deployment (CI/CD) ensure both smooth and automated deployment cycles.

| Tool                            | Role in CI/CD                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------- |
| **GitHub Actions**              | Automates testing, linting, and build processes when new commits are pushed.          |
| **Docker**                      | Standardizes the app environment, ensuring consistent builds across machines.         |
| **Heroku / AWS / DigitalOcean** | Hosts the application, with deployments triggered automatically from CI/CD pipelines. |

**Benefits:**

- Reduces manual deployment errors.

- Ensures fast feedback through automated testing.

- Keeps production code stable and up-to-date.

**Author and Repository**

- GitHub Repository: https://github.com/Iori-Watatsu/airbnb-clone-project
- Maintainer: Kamohelo Tshabalala
- Role: Backend Developer and Security Analyst

**Next Steps**

- Set up the initial Django project structure.

- Create models for Users, Properties, Bookings, Reviews, and Payments.

- Build RESTful API endpoints.

- Implement JWT authentication.

- Configure Docker and CI/CD pipelines.