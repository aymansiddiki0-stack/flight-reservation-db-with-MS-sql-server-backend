# Flight Reservation Database with MS SQL Server Backend
This project is a complete Flight Reservation System designed and built from scratch using Microsoft Access and SQL Server. It includes every layer of the system; from database entities and relationships to a fully functional Access frontend with VBA-driven forms, reports, and logic. The backend was later migrated to Microsoft SQL Server through SQL Server Migration Assistant (SSMA), creating a scalable and production-ready environment managed in SQL Server Management Studio (SSMS).

## Tech Stack
- Frontend: Microsoft Access (Forms, Reports, VBA)
- Backend: Microsoft SQL Server (T-SQL)
- Migration Tool: SQL Server Migration Assistant (SSMA)
- Tools: SSMS, ODBC DSN, VBA Editor, Git
- Environment: Windows 11

## Key Features
- #### Full Database Design
    - Designed a normalized relational schema covering flights, customers, bookings, routes, payments, and staff. Each table includes well-defined primary and foreign keys, ensuring strong referential integrity and minimal redundancy.

- #### Access Frontend with VBA Logic
    - The Access frontend features interactive forms, buttons, and navigation menus powered by VBA. All CRUD operations (create, update, delete) are handled dynamically, with validation and visual feedback built into the form workflows.

- #### Reports and Dashboards
    - Developed detailed Access reports summarizing bookings, flight schedules, and customer activity. These reports are visually formatted for readability and generated directly from live SQL Server data.

- #### SQL Server Integration
    - The Access backend was migrated to SQL Server using SSMA, with all tables, data, and constraints preserved. The frontend connects to SQL Server in real time through an ODBC DSN configuration, enabling faster performance and multi-user scalability.

- #### Visual Documentation
    - The repository includes screenshots of the entire process — from ER diagram design to migration validation and final Access UI screens.

## Backend Development in SSMS

After migration, all backend management and testing were performed in SQL Server Management Studio (SSMS):
- Created and configured the FlightReservationDB database, verifying that all tables, indexes, and constraints migrated correctly.
- Ran SQL queries to validate data integrity and relationship mappings between flights, customers, and bookings.
- Wrote and executed stored procedures for booking lookups, flight availability, and revenue summaries.
- Optimized table indexes to improve query performance and ensured that foreign key constraints enforced consistent referential integrity.
- Managed user permissions and authentication for Access frontend connectivity via ODBC.

This ensured the backend was robust, secure, and fully aligned with the Access interface’s business logic.

## Database Overview

### Core Entities
- Flights: Details of routes, aircrafts, departure, and arrival times
- Customers: Passenger records with personal and contact information
- Bookings: Links customers to their flights and tracks reservation details
- Payments: Stores transaction data and payment methods
- Routes: Defines the origin and destination for each flight
- Staff: Contains pilot and crew data

### Relationships

- One-to-many between Customers → Bookings
- One-to-many between Flights → Bookings
- One-to-one between Bookings → Payments

All constraints and dependencies are enforced in both Access and SQL Server.

### Screenshots for documentation include:
- Entity Relationship Diagram	
- Linked Tables after Migration	
- ODBC DSN Configuration	
- Access Customer Forms

More screenshots, including form designs and reports, can be found in the Screenshots/Forms/ directory.

## Setup (Quick Start)
- Clone the repository:
    - git clone https://github.com/aymansiddiki0-stack/flight-reservation-db-with-MS-sql-server-backend.git

- Open the Access frontend file located in
Access Frontend/Flight Reservation DB Migrated.accdb.
- Make sure your ODBC DSN is configured to connect to your SQL Server instance.
- Launch Access and open any form (e.g., CustomerForm, BookingForm) to interact with the live backend.
- The SQL schema can also be viewed or re-imported in SSMS using the included placeholder.sql file.

(It is a good idea to test the connection checking if the entries match up and if changes show up both ways)

Edits made in Access forms should appear instantly in SQL Server tables.

## License

MIT License 
