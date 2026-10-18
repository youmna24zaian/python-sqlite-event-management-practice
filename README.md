# Event Management Database Practice

![Project Banner](images/project-banner.png)

A hands-on database practice project using **Python and SQLite** to explore relational database design, SQL queries, data aggregation, and financial reporting through an event management scenario.

The project simulates an event management system that stores staff information, event details, and staff assignments. It demonstrates how to retrieve, analyze, and summarize relational data using SQL queries executed through Python's built-in `sqlite3` module.

## Project Overview

The database models an event management business, connecting employees with events and tracking their roles, working hours, hourly rates, and event budgets.

The project focuses on practical SQL skills, from basic relational operations to more advanced analytical queries.

## Database Structure

The database consists of three related tables:

| Table | Description |
|---|---|
| `Staff` | Stores employee information, including department, monthly salary, and hire date. |
| `Events` | Stores event details, including event name, client, type, budget, and date. |
| `EventAssignments` | Connects staff members to events and records their roles, hours worked, and hourly rates. |

The `EventAssignments` table uses foreign keys to connect staff members and events, establishing relationships between the three tables.

![Database Workflow](images/database-workflow.png)

## Technologies Used

- **Python** — Database interaction and query execution.
- **SQLite** — Relational database management.
- **SQL** — Data retrieval, joins, aggregation, subqueries, views, and common table expressions (CTEs).
- **Jupyter Notebook** — Organizing and documenting the practice exercises.

The project uses Python's built-in `sqlite3` module, so no third-party Python packages are required.

## Python–SQLite Connection Workflow

The notebook demonstrates how Python connects to a SQLite database and executes SQL statements using a database connection and cursor.

![Python Database Connection and Cursor Flow](images/python_db_connection_cursor_flow.png)

The basic workflow includes:

1. Importing the `sqlite3` module.
2. Connecting to the database using `sqlite3.connect()`.
3. Creating a cursor using `connection.cursor()`.
4. Executing SQL statements with `cursor.execute()`.
5. Retrieving query results using `cursor.fetchall()`.

## SQL Concepts Practiced

![SQL Concepts](images/sql-concepts.png)

The notebook covers the following SQL concepts through practical exercises:

- **Table Creation:** Creating relational tables with primary keys, foreign keys, and constraints.
- **Data Insertion:** Populating tables with sample staff, event, and assignment records.
- **JOIN Operations:** Combining related data across multiple tables.
- **Calculated Columns:** Computing assignment payments using hours worked multiplied by hourly rate.
- **Aggregate Functions:** Using `COUNT()`, `SUM()`, and `AVG()` to summarize data.
- **GROUP BY and HAVING:** Grouping records and filtering aggregated results.
- **DISTINCT:** Counting unique staff members and events.
- **Correlated Subqueries:** Comparing an assignment's hourly rate with the average rate for its event.
- **Subqueries and Nested Aggregation:** Identifying events with the highest total staff costs.
- **Views:** Creating an `EventFinancialSummary` view to analyze event budgets and remaining balances.
- **Common Table Expressions (CTEs):** Using `StaffWorkload` to analyze employee workloads.
- **Multiple CTEs:** Combining `StaffEventSummary` and `DepartmentAverage` to compare employee earnings against department averages.

## Key Query Exercises

The notebook contains eight main SQL exercises:

1. **Assignment Payment Analysis** — Join staff, events, and assignments, calculate total payments, and sort assignments by payment.
2. **Event Staff Cost Analysis** — Calculate assigned staff counts, total hours, average hourly rates, and total staff costs for each event.
3. **Department Performance Analysis** — Compare departments by participating staff, events, hours worked, and total earnings.
4. **Hourly Rate Comparison** — Identify assignments with hourly rates above the average for their respective events.
5. **Highest-Cost Event Identification** — Find the event or events with the highest total staff cost using a subquery.
6. **Event Financial Summary** — Create a view containing event details, staff costs, and remaining budgets.
7. **Staff Workload Analysis** — Identify staff members who worked on at least two events and more than 200 hours in total.
8. **Department Earnings Comparison** — Use two CTEs to identify staff members whose total event earnings exceed their department's average.

## Getting Started

### Prerequisites

- Python 3
- Jupyter Notebook or JupyterLab

SQLite is included with Python through the standard-library `sqlite3` module. No additional database server or third-party Python packages are required.

### Run the Project

1. Clone this repository:

   ```bash
   git clone https://github.com/youmna24zaian/python-sqlite-event-management-practice.git
   ```

2. Navigate to the project directory:

   ```bash
   cd python-sqlite-event-management-practice
   ```

3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `event_management_database_practice.ipynb`.

5. Run the notebook cells in order to create the database tables, insert the sample data, and execute the SQL exercises.

**Note:** The notebook connects to a SQLite database named `Online_Course`. SQLite will create the database file when the connection is opened if it does not already exist. Running the notebook repeatedly may require handling existing tables, records, or views appropriately.

## Repository Structure

```text
python-sqlite-event-management-practice/
├── images/
│   ├── project-banner.png
│   ├── database-workflow.png
│   ├── python_db_connection_cursor_flow.png
│   └── sql-concepts.png
├── .gitignore
├── README.md
├── requirements.txt
└── event_management_database_practice.ipynb
```

## Learning Objectives

- Understand relational database structure and table relationships.
- Practice writing SQL queries from business requirements.
- Analyze staff workloads, event costs, and department earnings.
- Apply joins, aggregate functions, subqueries, views, and CTEs.
- Integrate Python with SQLite for database operations.

---

**Project Type:** Database & SQL Practice

**Primary Technologies:** Python, SQLite, SQL, Jupyter Notebook# Event Management Database Practice

![Project Banner](images/project-banner.png)

A hands-on database practice project using **Python and SQLite** to explore relational database design, SQL queries, data aggregation, and financial reporting through an event management scenario.

The project simulates an event management system that stores staff information, event details, and staff assignments. It demonstrates how to retrieve, analyze, and summarize relational data using SQL queries executed through Python's built-in `sqlite3` module.

## Project Overview

The database models an event management business, connecting employees with events and tracking their roles, working hours, hourly rates, and event budgets.

The project focuses on practical SQL skills, from basic relational operations to more advanced analytical queries.

## Database Structure

The database consists of three related tables:

| Table | Description |
|---|---|
| `Staff` | Stores employee information, including department, monthly salary, and hire date. |
| `Events` | Stores event details, including event name, client, type, budget, and date. |
| `EventAssignments` | Connects staff members to events and records their roles, hours worked, and hourly rates. |

The `EventAssignments` table uses foreign keys to connect staff members and events, establishing relationships between the three tables.

![Database Workflow](images/database-workflow.png)

## Technologies Used

- **Python** — Database interaction and query execution.
- **SQLite** — Relational database management.
- **SQL** — Data retrieval, joins, aggregation, subqueries, views, and common table expressions (CTEs).
- **Jupyter Notebook** — Organizing and documenting the practice exercises.

The project uses Python's built-in `sqlite3` module, so no third-party Python packages are required.

## Python–SQLite Connection Workflow

The notebook demonstrates how Python connects to a SQLite database and executes SQL statements using a database connection and cursor.

![Python Database Connection and Cursor Flow](images/python_db_connection_cursor_flow.png)

The basic workflow includes:

1. Importing the `sqlite3` module.
2. Connecting to the database using `sqlite3.connect()`.
3. Creating a cursor using `connection.cursor()`.
4. Executing SQL statements with `cursor.execute()`.
5. Retrieving query results using `cursor.fetchall()`.

## SQL Concepts Practiced

![SQL Concepts](images/sql-concepts.png)

The notebook covers the following SQL concepts through practical exercises:

- **Table Creation:** Creating relational tables with primary keys, foreign keys, and constraints.
- **Data Insertion:** Populating tables with sample staff, event, and assignment records.
- **JOIN Operations:** Combining related data across multiple tables.
- **Calculated Columns:** Computing assignment payments using hours worked multiplied by hourly rate.
- **Aggregate Functions:** Using `COUNT()`, `SUM()`, and `AVG()` to summarize data.
- **GROUP BY and HAVING:** Grouping records and filtering aggregated results.
- **DISTINCT:** Counting unique staff members and events.
- **Correlated Subqueries:** Comparing an assignment's hourly rate with the average rate for its event.
- **Subqueries and Nested Aggregation:** Identifying events with the highest total staff costs.
- **Views:** Creating an `EventFinancialSummary` view to analyze event budgets and remaining balances.
- **Common Table Expressions (CTEs):** Using `StaffWorkload` to analyze employee workloads.
- **Multiple CTEs:** Combining `StaffEventSummary` and `DepartmentAverage` to compare employee earnings against department averages.

## Key Query Exercises

The notebook contains eight main SQL exercises:

1. **Assignment Payment Analysis** — Join staff, events, and assignments, calculate total payments, and sort assignments by payment.
2. **Event Staff Cost Analysis** — Calculate assigned staff counts, total hours, average hourly rates, and total staff costs for each event.
3. **Department Performance Analysis** — Compare departments by participating staff, events, hours worked, and total earnings.
4. **Hourly Rate Comparison** — Identify assignments with hourly rates above the average for their respective events.
5. **Highest-Cost Event Identification** — Find the event or events with the highest total staff cost using a subquery.
6. **Event Financial Summary** — Create a view containing event details, staff costs, and remaining budgets.
7. **Staff Workload Analysis** — Identify staff members who worked on at least two events and more than 200 hours in total.
8. **Department Earnings Comparison** — Use two CTEs to identify staff members whose total event earnings exceed their department's average.

## Getting Started

### Prerequisites

- Python 3
- Jupyter Notebook or JupyterLab

SQLite is included with Python through the standard-library `sqlite3` module. No additional database server or third-party Python packages are required.

### Run the Project

1. Clone this repository:

   ```bash
   git clone https://github.com/youmna24zaian/python-sqlite-event-management-practice.git
   ```

2. Navigate to the project directory:

   ```bash
   cd python-sqlite-event-management-practice
   ```

3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `event_management_database_practice.ipynb`.

5. Run the notebook cells in order to create the database tables, insert the sample data, and execute the SQL exercises.

**Note:** The notebook connects to a SQLite database named `Online_Course`. SQLite will create the database file when the connection is opened if it does not already exist. Running the notebook repeatedly may require handling existing tables, records, or views appropriately.

## Repository Structure

```text
python-sqlite-event-management-practice/
├── images/
│   ├── project-banner.png
│   ├── database-workflow.png
│   ├── python_db_connection_cursor_flow.png
│   └── sql-concepts.png
├── .gitignore
├── README.md
├── requirements.txt
└── event_management_database_practice.ipynb
```

## Learning Objectives

- Understand relational database structure and table relationships.
- Practice writing SQL queries from business requirements.
- Analyze staff workloads, event costs, and department earnings.
- Apply joins, aggregate functions, subqueries, views, and CTEs.
- Integrate Python with SQLite for database operations.

---

**Project Type:** Database & SQL Practice

**Primary Technologies:** Python, SQLite, SQL, Jupyter Notebook
