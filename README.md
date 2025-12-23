[日本語はこちら](README-ja.md)

# Small-Business-Operations-Platform-Project

The goal of this project is **not just to build an app**, but to:
- Learn **SQL, data modeling, and reporting**
- Learn **backend development using Go**
- Implement **basic frontend development using HTML and CSS**
- Understand how **real internal tools** are designed and used in companies

This project intentionally mirrors:
- POS backends
- Admin dashboards
- Inventory systems
- Payroll & staff tracking tools

---

## ☕︎ Why This Project Exists

Many companies already have customer-facing applications.
What they need — and struggle to maintain — are **internal tools**.

This project demonstrates the ability to:
- Design structured data
- Implement business logic
- Build CRUD systems
- Generate reports using SQL
- Connect frontend interfaces to backend services

---

## ✎ Skills Learned in This Project

### Tech Skills
- SQL (tables, joins, aggregates, indexes)
- Go (HTTP servers, handlers, structs)
- HTML (forms, tables)
- CSS (layout, usability)
- REST APIs
- Database migrations

### Concept Skills
- Data normalization
- Relational thinking
- Business logic modeling
- Role-based access
- System design fundamentals

---

## ★ System Description

The system is designed for **internal use only** and supports three user roles:

### Roles
- **Admin** – Full access
- **Manager** – Inventory, reports, staff management
- **Staff** – Clock in/out, view schedule

---

## 📦 Core Features

### 1. Staff Management
- Add/edit staff members
- Assign roles and hourly rates

### 2. Time Tracking
- Clock in / clock out
- Store shift records
- Prepare data for payroll calculation

### 3. Payroll Reporting
- Calculate hours worked
- Generate pay summaries per period

### 4. Inventory Management
- Track stock quantities
- Set reorder thresholds
- Update inventory based on sales

### 5. Menu / Item Management
- Food and drink items
- Cost vs price tracking
- Category classification

### 6. Sales Logging
- Record orders
- Link items to sales
- Track daily revenue

### 7. Reporting Dashboard
- Revenue by day
- Top-selling items
- Labor cost vs sales

---

## 🗄 Database Design Philosophy

### Rules Followed:
- Each table represents **one entity**
- Each row represents **one record**
- IDs are used instead of names
- **No duplicated data**

---

## 🧾 Database Tables (Initial Design)

### Staff
```sql
staff_id (PK)
first_name
last_name
role
hourly_rate
```

### Timecards
```sql
timecard_id (PK)
staff_id (FK)
clock_in
clock_out
work_date
```

### poayroll
```sql
payroll_id (PK)
staff_id (FK)
pay_period
hours_worked
total_pay
```

etc

## 🖥 Frontend 

Non Complex frameworks

Technologies Used:

HTML (forms, tables)

CSS (basic layout, readability)

Focus:

Clear data display

Simple navigation

Functional and easy to use UI

## ⚙ Backend Architecture (Go)
Responsibilities:

Handle HTTP requests

Validate data

Execute SQL queries

Return HTML or JSON responses

