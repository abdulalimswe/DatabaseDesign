# Task Management System - Database Design

## Overview
This repository contains the database design artifacts for a Task Management System, including requirements, entity analysis, relationships, ER diagram, table design, schema, SQL statements, and normalization.

## Contents
- `Diagram/` - Design diagrams and the source PDF
- `schema.sql` - PostgreSQL-compatible schema

## System Goals
The system helps individuals and teams plan, organize, and track tasks efficiently, improving productivity and meeting deadlines.

## Users / Stakeholders
- Individual Users - manage their own tasks
- Team Members - collaborate on shared tasks
- Admin (optional) - manage users and system settings

## Core Features (MVP)
- User management: register, login/logout, profile updates
- Task management: create, view, edit, delete
- Task status: To Do, In Progress, Done
- Due date tracking: set and view upcoming tasks
- Comments: add and view task discussions
- Notifications: due date reminders, task assignments, status changes

## Entities
- **Users**
- **Tasks**
- **Comments**
- **Notifications**
- **Task Statuses** (lookup)
- **Notification Types** (lookup)

## Relationships
- User -> Task (1:M)
- Task -> Comment (1:M)
- User -> Notification (1:M)
- Task -> Status (M:1)
- Notification -> Type (M:1)

## Diagrams

### 1) Requirements Analysis
![Requirements Analysis](Diagram/01.%20Requirements%20Analysis.png)

### 2) Entity Thinking
![Entity Thinking](Diagram/02.%20Entity%20Thinking.png)

### 3) Relationship Diagram
![Relationship Diagram](Diagram/03.%20Relationship%20Diagram.png)

### 3.1) Relationship Diagram (Detailed)
![Relationship Diagram Detailed](Diagram/03.1%20Relationship%20Diagram.png)

### 4) ER Diagram
![ER Diagram](Diagram/04.%20ER%20Diagram.png)

### 5) Table Design
![Table Design](Diagram/05.%20Table%20Design.png)

### 6) Schema Design
![Schema Design](Diagram/06.%20Schema%20Design.png)

### 6.1) SQL Schema Command
![SQL Schema Command](Diagram/06.1%20SQL%20Schema%20Command.png)

### 7) Normalization
![Normalization](Diagram/07.%20Normalization.png)

## SQL Schema
The SQL schema lives in `schema.sql` and is compatible with PostgreSQL. It includes:
- Auto-incrementing primary keys
- Foreign key constraints with cascade deletes
- Indexes for common queries
- Seed data for task statuses and notification types

## Normalization Summary
All tables are normalized to **Third Normal Form (3NF)**:
- **1NF**: atomic columns, no repeating groups
- **2NF**: no partial dependencies
- **3NF**: no transitive dependencies

## Source PDF
The full design report is provided in:
- `Diagram/Database Design - Task Management System.pdf`
