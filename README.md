
# Software Requirement Specification (SRS) Document
## Network Ticketing Management System
### Project Name: Network Ticketing for Customer Inventory Data
### Author: Srivasthavi Mannepula
### Date: October 10, 2023

---

## Table of Contents

1. **Introduction**
   1.1 Purpose
   1.2 Scope
   1.3 Definitions, Acronyms, and Abbreviations
   1.4 References
   1.5 Overview

2. **Functional Requirements**
   2.1 User Roles
   2.2 User Authentication
   2.3 Incident Logging
   2.4 Network Element Selection
   2.5 Related Components
   2.6 Issue Reporting and Ticket Creation
   2.7 Assignment Group Selection
   2.8 Incident Creation
   2.9 Incident Resolution
   2.10 Root Cause Attribution
   2.11 Issue Tracking

3. **Non-Functional Requirements**
   3.1 Performance
   3.2 Security
   3.3 Usability
   3.4 Reliability

4. **Technical Details**
   4.1 Development Platform
   4.2 Database
   4.3 API
   4.4 Integration with Open Source Application Servers

5. **Appendices**
   5.1 Use Case Diagram
   5.2 Data Model
   5.3 Glossary

---

## 1. Introduction

### 1.1 Purpose
The Network Ticketing Management System (NTMS) aims to provide a comprehensive solution for managing incidents related to customer network inventory data. This document outlines the software requirements for NTMS.

### 1.2 Scope
The NTMS will allow users to log incidents, select network elements, report issues, create tickets, assign them to appropriate groups, manage incident resolution, and track the status of incidents. It will facilitate efficient incident management within the customer's network infrastructure.

### 1.3 Definitions, Acronyms, and Abbreviations
- NTMS: Network Ticketing Management System
- API: Application Programming Interface
- ITIL: Information Technology Infrastructure Library

### 1.4 References
- Basic incident management principles based on ITIL documentation.

### 1.5 Overview
This document provides a detailed specification of functional and non-functional requirements for the NTMS, along with technical details and appendices containing use case diagrams, user interface mockups, data models, and a glossary.

---

## 2. Functional Requirements

### 2.1 User Roles
The NTMS will support the following user roles with specific functionalities:

#### 2.1.1 Customer
- **Login**: Customers should be able to log in with their credentials.
- **Incident Logging**: Customers can log incidents against configuration items.
- **Network Element Selection**: Customers can search and select network elements (e.g., router, OLT, ONT) from the database.
- **Related Components**: Customers can view a list of related components deployed with the selected network element.
- **Issue Reporting and Ticket Creation**: Customers can report issues such as power problems, not reachable, port not working, and create corresponding tickets.
- **Incident Tracking**: Customers can view the status and progress of incidents they've reported.
- **User Profile**: Customers can update their profile information.

#### 2.1.2 Support Agent
- **Login**: Support agents should be able to log in with their credentials.
- **Incident Management**: Support agents can manage incidents reported by customers, including updating the status, assigning to specific groups, and resolving issues.
- **Incident Resolution**: Support agents can add resolution comments, attribute a root cause to the resolution, and update the incident's status.
- **Incident Assignment**: Support agents can assign incidents to specific groups based on the type and severity of the issue.
- **Incident Tracking**: Support agents can view and filter incidents by status, priority, and assignment group.
- **User Management**: Support agents can manage user accounts, including creating, updating, and deactivating accounts.
- **Reporting**: Support agents can generate incident reports based on various criteria such as date, severity, and resolution time.

### 2.2 User Authentication
- Users must provide valid credentials (username and password) to access the system.
- Passwords should be securely hashed and stored.
- Implement password recovery and reset mechanisms for forgotten passwords.

### 2.3 Incident Logging
- Users should be able to log incidents by providing details such as title, description, and affected network element.
- Attach files or relevant documentation to incidents if necessary.

### 2.4 Network Element Selection
- **Description**: Customers should have the ability to search for and select network elements (e.g., router, OLT, ONT) from the database. Network elements represent various hardware components within the customer's network infrastructure. This feature allows customers to pinpoint the specific component they want to report an issue on.

- **Example**: Consider a telecommunications company's network. A customer may want to report a connectivity issue with a particular router (Router A) located in their office. Using the Network Element Selection feature, they can search for "Router A" and select it from the list of available network elements, ensuring accurate incident reporting.

### 2.5 Related Components
- **Description**: This functionality allows customers to view a list of components related to the selected network element. Network elements are often part of a larger network topology, and knowing the related components can provide crucial context for troubleshooting and issue reporting.

- **Example**: Suppose a customer selects an Optical Line Terminal (OLT) as the network element. The Related Components feature would display a list of Optical Network Terminals (ONTs) and other devices connected to that OLT. This information helps the customer understand the network's structure and identify potential areas where issues might be occurring.

### 2.6 Issue Reporting and Ticket Creation
- **Description**: This capability enables customers to report issues related to the selected network element and create corresponding tickets for those issues. Customers can specify the type of issue they are facing (e.g., power problems, not reachable, port not working) and provide additional details.

- **Example**: Suppose a customer has selected a specific Optical Network Terminal (ONT) as the network element. They can use the Issue Reporting and Ticket Creation feature to report that the ONT is not reachable. In the description, they might mention that the ONT's indicator lights are off, indicating a power issue. Upon submission, the system generates a unique ticket ID (e.g., Ticket #12345), initiating the incident management process.

### 2.7 Assignment Group Selection
- Define assignment rules based on the issue type, severity, and other criteria.
- Automatically assign incidents to the appropriate support groups or agents.

### 2.8 Incident Creation
- When a ticket is created, record the following information:
  - Severity: Define severity levels (e.g., critical, high, medium, low).
  - Priority: Assign priority levels based on business rules.
  - Timestamps: Capture creation and last update timestamps.

### 2.9 Incident Resolution
- Support agents can work on assigned incidents.
- Record actions taken, resolution comments, and updates to the incident status.
- Include fields for tracking time spent on resolution.

### 2.10 Root Cause Attribution
- Allow support agents to attribute a root cause to the incident resolution.
- Categorize root causes for later analysis and improvement.

### 2.11 Issue Tracking
- Provide a dashboard displaying a list of incidents in various states, including open, in progress, and resolved.
- Enable users to filter and sort incidents based on different criteria.
- Implement notifications to inform users of incident updates.

---

## 3. Non-Functional Requirements

### 3.1 Performance
- The system should respond to user actions within seconds.
- Handle concurrent users efficiently.

### 3.2 Security
- Ensure secure user authentication.
- Protect sensitive customer inventory data.

### 3.3 Usability
- The user interface should be intuitive and user-friendly.
- Provide error messages and guidance for users.

### 3.4 Reliability
- Ensure system availability 24/7.
- Implement regular backups and disaster recovery procedures.

---

## 4. Technical Details

### 4.1 Development Platform
- Frontend: Angular-ReactJS
- Backend: Open-source Application Servers

### 4.2 Database
- Use any open-source database to store customer network inventory data securely.

### 4.3 API
- Develop APIs for communication between frontend and backend components.

### 4.4 Integration with Open Source Application Servers
- Integrate NTMS with open-source application servers for scalability and performance.

---
