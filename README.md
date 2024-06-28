# Airport Management System ER Diagram and Relational Schema

## Overview

This document provides the Entity-Relationship (ER) Diagram and Relational Schema for an Airport Management System. It outlines the structure of the database, detailing the various entities, their attributes, and the relationships between them.

## Contents

1. **ER Diagram**
   - Visual representation of the entities, their attributes, and the relationships among them.
2. **Relational Schema**
   - Tabular representation of the entities and their attributes, including primary keys and foreign keys.

## ER Diagram

The ER Diagram provides a graphical representation of the database structure, including:

- **Entities**: Major components such as `Airports`, `Flights`, `Passengers`, `Employees`, etc.
- **Attributes**: Characteristics of the entities like `airport_id`, `flight_number`, `passenger_name`, `employee_id`, etc.
- **Relationships**: Associations between the entities, such as `Flights` being operated from one `Airport` to another, `Passengers` booking `Flights`, `Employees` managing `Airports`, etc.

## Relational Schema

The Relational Schema provides a detailed tabular representation, including:

- **Tables**: Each entity is represented as a table.
- **Columns**: Attributes of the entities are represented as columns in the tables.
- **Primary Keys**: Unique identifiers for each entity (e.g., `airport_id` for `Airports`).
- **Foreign Keys**: Links between entities (e.g., `airport_id` in `Flights` linking to `Airports`).

### Example

- **Airports Table**
  - `airport_id` (Primary Key)
  - `airport_name`
  - `location`

- **Flights Table**
  - `flight_number` (Primary Key)
  - `departure_airport_id` (Foreign Key referencing `Airports`)
  - `arrival_airport_id` (Foreign Key referencing `Airports`)
  - `departure_time`
  - `arrival_time`

- **Passengers Table**
  - `passenger_id` (Primary Key)
  - `passenger_name`
  - `flight_number` (Foreign Key referencing `Flights`)

- **Employees Table**
  - `employee_id` (Primary Key)
  - `employee_name`
  - `airport_id` (Foreign Key referencing `Airports`)

## Usage

This document is intended for use by database administrators, developers, and analysts involved in the design, implementation, and maintenance of the Airport Management System.


## Notes

- Ensure that the database constraints and relationships are correctly implemented to maintain data integrity.
- Regular updates to the schema might be necessary to accommodate changes in business requirements or processes.
