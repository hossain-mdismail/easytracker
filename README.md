# EasyTracker 

EasyTracker is a modern, lightweight personal finance tracking web application built with **FastAPI**, **SQLAlchemy**, and a **PostgreSQL** database, featuring a clean, responsive black-and-white minimalist frontend.

---

##  Key Features

* **Secure Authentication**: User registration and login powered by **JWT (JSON Web Tokens)** with a 7-day session duration, and password hashing via `passlib` and `bcrypt`.
* **Private User Workspaces**: Strict data isolation ensuring each user only views, modifies, and deletes their own financial records.
* **Flexible Transaction Entry**: 
  * *Single Entry Form*: Quickly add income or expenses with custom categories, accounts, and dates.
  * *Smart Batch Paste*: Paste raw daily logs to have them automatically parsed and saved in bulk.
* **Financial Summary & Calculations**: Real-time tracking of total income, total expenses, and net savings or deficits with dynamic status indicators.
* **Advanced Filtering & UI Controls**: 
  * Custom date range filtering (From/To).
  * 3-state table row limit toggle (5 records, 20 records, or All).
  * Multi-currency support (USD, EUR, GBP, PKR, etc.) saved locally in the browser.
* **Undo Functionality**: Floating toast notification with an **Undo** action for recently added or deleted transactions.

---

##  Tech Stack

* **Backend**: Python, FastAPI, SQLAlchemy, PostgreSQL, PyJWT, Passlib, Uvicorn
* **Frontend**: HTML5, Vanilla JavaScript, CSS3 (Modern Flexbox/Grid Minimalist Design)

---

##  Project Structure

```text
easyTracker/
├── main.py              # FastAPI application, auth logic, and API endpoints
├── models.py            # SQLAlchemy database models (User & Transaction)
├── database.py          # PostgreSQL database connection setup
├── parser.py            # Natural language/raw text transaction parser
├── index.html           # Minimalist frontend interface & client-side logic
├── recover_data.py      # Data migration utility script for user assignment
├── .env.example         # Environment variables template
└── .gitignore           # Git ignore configuration
