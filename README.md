# Library Management System

## Project Overview
**Project 01: Library Management System**  
**DATCOM Lab**  
**NEU-College of Technology**  
**National Economics University**  
**Contact:** hung.tran@neu.edu.vn

### Objective
The objective of this project is to develop an effective digital system for managing library operations, optimizing the borrowing and returning processes, and enhancing user experience through an efficient information retrieval and management system.

---

## Tech Stack
- **Database Management System:** MySQL
- **Programming Language:** Python
- **Libraries:** `mysql-connector-python` or `SQLAlchemy`

---

## System Features

### Core Functionalities
- **Book Management:** Add, edit, delete, and search books.
- **Category & Author Management:** Maintain detailed records of book categories and authors.
- **Reader Management:** Register new readers and update existing reader information.
- **Borrowing & Returning:** Manage the complete lifecycle of book loans.
- **Overdue Alerts:** Automated notifications for overdue books.
- **Statistical Reporting:** Generate reports on book inventory and reader activity.

### Database Capabilities
- **Advanced Objects:**
  - **Indexes:** Optimized for fast query performance.
  - **Views:** Pre-defined queries for quick reporting.
  - **Stored Procedures:** Handle complex logic like borrowing transactions and overdue calculations.
  - **User Defined Functions (UDFs):** Custom data processing.
  - **Triggers:** Automatically update book quantities upon borrowing or returning.
- **Security & Administration:**
  - User management and role-based permissions.
  - Data security protocols.
  - Backup and recovery strategies.
  - Performance optimization.

---

## Database Schema

### Entity Relationship
The system is built on a relational model converting ER diagrams into the following schema:

| Table | Columns |
| :--- | :--- |
| **Books** | `BookID`, `BookName`, `AuthorID`, `PublishYear`, `Quantity`, `CategoryID` |
| **Categories** | `CategoryID`, `CategoryName` |
| **Authors** | `AuthorID`, `AuthorName` |
| **Readers** | `ReaderID`, `ReaderName`, `Address`, `PhoneNumber` |
| **Borrowing** | `BorrowID`, `ReaderID`, `BookID`, `BorrowDate`, `ReturnDate` |

*Note: The database includes 5-10 sample records per table for testing.*

---

## Installation & Setup

### Prerequisites
- Python 3.x installed
- MySQL Server installed and running
- `pip` package manager

### 1. Database Setup
1. Create the database in MySQL:
   ```sql
   CREATE DATABASE LibraryDB;
   USE LibraryDB;
   ```
2. Run the provided SQL scripts to create tables, views, stored procedures, and triggers.
3. Insert sample data using the provided initialization script.

### 2. Python Environment
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```
2. Install dependencies:
   ```bash
   pip install mysql-connector-python
   # OR
   pip install sqlalchemy
   ```
3. Configure database connection settings in the application configuration file (e.g., `config.py`):
   ```python
   DB_CONFIG = {
       'host': 'localhost',
       'user': 'your_username',
       'password': 'your_password',
       'database': 'LibraryDB'
   }
   ```

### 3. Running the Application
Run the main Python script to launch the console interface:
```bash
python main.py
```

---

## Project Structure
```text
.
├── README.md
├── requirements.txt
├── database/
│   ├── schema.sql          # Table definitions
│   ├── procedures.sql      # Stored procedures & triggers
│   └── seed_data.sql       # Sample data insertion
├── src/
│   ├── config.py           # Database configuration
│   ├── db_connector.py     # Database connection logic
│   ├── book_manager.py     # Book CRUD operations
│   ├── reader_manager.py   # Reader management
│   ├── loan_manager.py     # Borrow/Return logic
│   └── reports.py          # Statistical reporting
└── docs/
    └── diagrams/           # ER Diagrams and MySQL Workbench exports
```

---

## Deliverables
- Complete project report (20-30 pages) covering analysis, design, implementation, and conclusions.
- Database diagrams (ERD).
- SQL Scripts for schema, objects, and data.
- Python source code for the application.

---

## Conclusion & Recommendations
This project evaluates the effectiveness of digital library management. Future improvements may include:
- Migration to a GUI-based interface (e.g., Tkinter, PyQt).
- Web-based deployment.
- Integration with barcode/RFID scanners.
- Advanced analytics dashboards.

---

## References
- National Economics University Project Guidelines.
- MySQL Official Documentation.
- Python Database API Specification v2.0.

---

## License
This project is developed for educational purposes at the National Economics University.

