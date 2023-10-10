# Software Requirements Specification (SRS)
## Billing System - 3rd Party Services

### Table of Contents
1. [Introduction](#1-introduction)
2. [System Overview](#2-system-overview)
3. [Functional Requirements](#3-functional-requirements)
4. [Non-Functional Requirements](#4-non-functional-requirements)
5. [System Constraints](#5-system-constraints)
6. [Assumptions and Dependencies](#6-assumptions-and-dependencies)

### 1. Introduction
The Software Requirements Specification (SRS) document outlines the requirements for the "Billing System - 3rd Party Services" project. This application is designed for the billing of third-party services, such as Disney Hotstar and Netflix, within a family mobile account.

#### Author/Owner
Prashant

#### Project Name
Billing System - 3rd Party Services

#### Description
The Billing System - 3rd Party Services is an application designed for billing and managing third-party services subscriptions within a family mobile account. It includes functionality for creating a customer account hierarchy, adding third-party services, processing bulk invoices, generating user invoices, and handling payments and service suspensions.

### 2. System Overview
The system allows for the creation of a customer account hierarchy for family mobile accounts, adding third-party services to billing accounts, processing bulk invoices from third-party providers, generating user invoices, and managing payments and service suspensions.

### 3. Functional Requirements
| Requirement | Description | Software Requirements |
|-------------|-------------|-----------------------|
| 1. Create Customer Account Hierarchy | The system shall allow the creation of a customer account hierarchy for family mobile accounts, where 4 to 5 mobile services can be grouped under one billing account. | Frontend: Angular, Backend: Spring Boot, Microservices |
| 2. Add 3rd Party Services | The system shall support the addition of 3rd party services, such as Disney Hotstar and Netflix subscriptions, to billing accounts. Third-party API stubs shall be created to facilitate the addition of these services. | Frontend: Angular, Backend: Spring Boot, Microservices |
| 3. Bulk Invoice Processing | Every month, the system shall receive a bulk B2C invoice from third-party providers. The system shall process the invoice, generating individual invoices for users, and send them via email. | Backend: Spring Boot, Microservices, SQL Database |
| 4. User Invoice Viewing | Users shall be able to view their invoices within the application. | Frontend: Angular, Backend: Spring Boot, Microservices |
| 5. Payment Processing | Users shall be able to make payments for their total bills through the application. | Frontend: Angular, Backend: Spring Boot, Microservices, SQL Database |
| 6. Service Management | The provider shall have the ability to activate or deactivate 3rd party services based on invoice payment status. | Backend: Spring Boot, Microservices, SQL Database |
| 7. Scenarios | The system shall handle the following scenarios: 1. User makes an on-time payment. 2. User does not make payment - Services disrupted. 3. User makes payment post-disruption, and services are resumed. 4. Long payment due - Services terminated. | Backend: Spring Boot, Microservices |

### 4. Non-Functional Requirements
- Performance: The system shall meet performance criteria, including response times and scalability. Backend: Spring Boot, Frontend: Angular, SQL Database
- Security: The system shall implement security measures, including authentication and authorization. Backend: Spring Boot, Frontend: Angular
- Reliability: The system shall ensure high availability and provide backup and recovery mechanisms. Backend: Spring Boot, SQL Database
- Usability: The user interface shall be intuitive and user-friendly. Frontend: Angular
- Compatibility: The system shall be compatible with various devices and browsers. Frontend: Angular

### 5. System Constraints
- The system shall rely on API stubs for third-party service integration.
- The billing system shall run bill run services every 30 days.
- Microservices include Billing System, Invoice Generation, and Collection.
- Collection shall process payment input files daily and run collections cycles every 14 days.

### 6. Assumptions and Dependencies
- The system assumes the availability of third-party API stubs.
- Dependencies include the timely receipt of bulk invoices from third-party providers (stubs).

---

This Software Requirements Specification (SRS) document outlines the requirements for the "Billing System - 3rd Party Services" project. It serves as a reference for the development to ensure that the system is built to meet the specified functional and non-functional requirements.
