# Event Management Database Practice

A hands-on **Python and SQLite** practice project focused on relational data, SQL querying, and event-cost analysis.

The project models an event-management business using three related tables: staff, events, and event assignments. The notebook creates the tables, inserts sample data, and works through eight SQL exercises.

## Database Schema

| Table | Purpose |
|---|---|
| `Staff` | Staff names, departments, salaries, and hire dates |
| `Events` | Event names, clients, types, budgets, and dates |
| `EventAssignments` | Staff-to-event assignments, roles, hours, and hourly rates |

## Technologies

- **Python** — runs the SQL queries through the standard-library `sqlite3` module
- **SQLite** — stores the relational data locally
- **SQL** — joins, calculated columns, aggregate functions, subqueries, views, and CTEs
- **Jupyter Notebook** — organizes the exercises

No third-party Python packages are required for the database operations.

## SQL Exercises

The notebook contains eight exercises:

1. **Assignment payments:** join the three tables and calculate each assignment's total payment.
2. **Event staff costs:** summarize staff counts, hours, average rates, and total costs by event.
3. **Department performance:** compare departments by staff, events, hours, and earnings.
4. **Correlated subquery:** find assignments whose hourly rate exceeds the average for that event.
5. **Highest-cost event:** use a subquery to identify the event or events with the greatest staff cost.
6. **Financial summary view:** calculate event staff costs and remaining budgets.
7. **Staff workload CTE:** find staff who worked on at least two events and more than 200 hours.
8. **Department earnings comparison:** use two CTEs to compare each staff member's event earnings with their department average.

## Getting Started

### Requirements

- Python 3
- Jupyter Notebook or JupyterLab

### Run the notebook

1. Clone the repository:

   ```bash
   git clone https://github.com/youmna24zaian/python-sqlite-event-management-practice.git
   ```

2. Open the project folder:

   ```bash
   cd python-sqlite-event-management-practice
   ```

3. Start Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open `event_management_database_practice.ipynb` and run its cells in order.

The notebook creates a local SQLite database named `Online_Course` in the current working directory. Run the exercises against a fresh database for the first run; rerunning the data-insertion cells may raise primary-key errors because the sample records are inserted with fixed IDs.

## Repository Contents

- `event_management_database_practice.ipynb` — database setup, sample data, and eight SQL exercises
- `images/` — project diagrams used in the documentation
- `.gitignore` — excludes local Python artifacts and the generated database file

## Learning Goals

- Design related tables with primary and foreign keys
- Write multi-table joins and analytical SQL queries
- Summarize data with aggregate functions and grouping
- Use correlated subqueries, nested aggregation, views, and CTEs
- Connect Python code to a local SQLite database

---

**Project type:** Python, SQLite, and SQL practice
