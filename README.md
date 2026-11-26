# Cloud-Based Smart Parking Management System

**Course:** Cloud Infrastructure and Services (25CS2206E)  
**Academic Year:** 2026–2027  
**Project Type:** CDIS Project – Proposed System

## Team Details

| S. No. | Team Member | Roll Number |
|---:|---|---|
| 1 | G. ROHITH | 2520030220 |
| 2 | P. ANUDEEP | 2520030087 |
| 3 | SAMBAVARAM SARVESWARA REDDY | 2520030049 |

## Project Guide

- **Professor / Guide Name:** Dr. S. Vinay Kumar
- **Designation:** Associate Professor
- **Department:** Computer Science and Engineering

## Abstract

The Cloud-Based Smart Parking Management System aims to simplify parking operations by providing a centralized platform for monitoring parking slot availability, registering vehicle entry and exit, reserving slots, and generating parking utilization reports. Simulated sensor data will update slot occupancy dynamically, enabling users to identify available spaces and reducing the time spent searching for parking.

The system will maintain vehicle records, reservation details, and parking transaction history in a persistent relational database. The application will be packaged using Docker containers and deployed on Amazon EC2 instances. EC2 Auto Scaling and an Application Load Balancer will distribute incoming requests and adjust computing capacity according to demand.

Amazon VPC will provide a secure network architecture through planned IP address ranges, public and private subnets, and security groups. Amazon RDS for MySQL will provide persistent storage, while AWS IAM will control access to cloud resources. Amazon CloudWatch dashboards, logs, and alarms will monitor parking transactions, application response times, and infrastructure health.

The expected outcome is a scalable, reliable, and secure parking management platform that improves space utilization, minimizes manual effort, and supports informed decision-making through occupancy and utilization reports.

## 1. Problem Statement

Traditional parking operations can create several difficulties:

- Drivers spend time searching for available parking spaces.
- Manual vehicle entry and exit tracking can be slow and error-prone.
- Parking operators may lack centralized visibility into parking utilization.
- Uncoordinated reservations can lead to inefficient use of parking spaces.

The proposed system addresses these issues through a centralized, cloud-hosted parking management platform.

## 2. Project Objectives

- Display available and occupied parking slots.
- Enable users to reserve parking spaces.
- Record vehicle entry and exit information.
- Simulate sensor-based updates to parking availability.
- Provide a centralized administrator dashboard.
- Maintain vehicle, reservation, and parking transaction records.
- Support cloud deployment, monitoring, and controlled access.

## 3. Proposed Solution

The system is organized around three main areas:

### User Portal
Users can view parking slots, select a space, reserve it, and review booking status.

### Parking Operations
The system records vehicle entry and exit details and updates slot occupancy.

### Admin Dashboard
Administrators can monitor parking occupancy, bookings, and usage trends.

## 4. High-Level System Workflow

1. A simulated sensor data generator sends a parking-slot status update.
2. The application validates the update and saves the occupancy status.
3. Users view available slots and submit a reservation.
4. Vehicle entry and exit events update the parking record.
5. The administrator dashboard displays parking utilization and activity.

**Note:** The project presentation describes simulated sensor updates. Physical IoT sensors are part of the future scope, not a stated current implementation.

## 5. Core Modules

| Module | Description |
|---|---|
| Authentication | Supports user/admin roles and controlled access. |
| Slot Management | Maintains slot status, location, and occupancy updates. |
| Reservation | Creates, displays, and manages parking bookings. |
| Vehicle Tracking | Records vehicle registration and entry/exit times. |
| Analytics | Provides administrators with occupancy and usage summaries. |

## 6. Conceptual Data Model

The proposed data model contains the following entities:

| Entity | Example attributes |
|---|---|
| Users | `user_id`, `name`, `role`, `contact` |
| Parking Slots | `slot_id`, `location`, `status` |
| Reservations | `reservation_id`, `user_id`, `slot_id`, `time`, `status` |
| Vehicles | `vehicle_id`, `plate_number`, `user_id` |
| Entry / Exit Logs | `log_id`, `vehicle_id`, `slot_id`, timestamps |

## 7. AWS Services and Cloud Technologies

The project abstract identifies these AWS services and technologies:

| Service / Technology | Purpose in the project |
|---|---|
| Amazon EC2 | Hosts the web application and backend APIs. |
| Amazon EC2 Auto Scaling | Adjusts EC2 capacity according to demand. |
| Elastic Load Balancing – Application Load Balancer | Distributes incoming application requests. |
| Amazon VPC | Provides an isolated network environment with planned IP ranges and subnets. |
| Amazon RDS for MySQL | Provides persistent relational database storage. |
| Amazon Elastic Container Registry (ECR) | Stores container images used for deployment. |
| AWS IAM | Controls access to AWS resources and services. |
| Amazon CloudWatch | Provides dashboards, logs, metrics, and alarms for monitoring. |
| Docker | Packages the application into containers. |

### Architecture note

The presentation's architecture slide describes the database as **RDS or DynamoDB** and says that the final database and application framework are to be finalized. The separate project abstract specifies **Amazon RDS for MySQL** and lists the additional AWS services above. The implementation should follow the final architecture approved by the project guide.

## 8. Testing Plan and Expected Outcomes

### Functional Testing
- Reservation creation.
- Parking availability updates.
- Vehicle entry and exit logging.
- User and administrator role access.

### Integration Testing
Check consistency across the following flow:

**Sensor Simulator → API → Database → Dashboard**

### Expected Outcomes
- Reduced time spent searching for parking.
- Clearer visibility of parking occupancy.
- More efficient parking operations.
- Better utilization reporting for administrators.

These are expected project benefits and should be validated through testing.

## 9. Implementation Plan

1. **Phase 1 – Planning:** Gather requirements, prepare wireframes, and design the database.
2. **Phase 2 – Development:** Build the user portal, backend APIs, and administrator dashboard.
3. **Phase 3 – Integration:** Integrate simulated sensor events and reservations.
4. **Phase 4 – Cloud Deployment:** Deploy to EC2 and configure CloudWatch and the other selected AWS services.
5. **Phase 5 – Testing and Documentation:** Test the system, evaluate results, and prepare project documentation.

## 10. Conclusion

The Cloud-Based Smart Parking Management System proposes a centralized platform connecting drivers and parking administrators. It is designed to display parking availability, support reservations, record vehicle entry and exit, and provide parking utilization information. Simulated sensor data enables the project to demonstrate dynamic slot updates without physical IoT hardware. AWS infrastructure is proposed for application deployment, data storage, security, scalability, and monitoring.

## 11. Future Scope

- Integration of real IoT parking sensors.
- Online parking payment integration.
- Predictive analytics for estimating parking demand.
- Further improvements to monitoring and parking utilization reports.

---

**Document basis:** Project presentation, *Cloud-Based Smart Parking Management System* (12 slides), and the uploaded *CDIS_Abstract.pdf* (2 pages).  
