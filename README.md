# FastAPI Bookstore API (with PostgreSQL)

A robust RESTful API for managing a bookstore inventory, built with **FastAPI**, **SQLAlchemy ORM**, **Pydantic**, and **PostgreSQL**.

---

## 🚀 Features

* **Full CRUD Operations:** Create, read, update, and delete books seamlessly.
* **Data Validation & Serialization:** Strict schema enforcement using Pydantic models.
* **Relational Persistence:** Database interactions using SQLAlchemy ORM with PostgreSQL.
* **Environment Configuration:** Secure credential management via `.env` files.
* **Interactive Documentation:** Automatically generated OpenAPI specs via Swagger UI and ReDoc.

---

## 🛠 Tech Stack

* **Framework:** FastAPI
* **Language:** Python 3.10+
* **Database:** PostgreSQL
* **ORM:** SQLAlchemy
* **ASGI Server:** Uvicorn
* **Validation:** Pydantic

---

## 📁 Project Structure

```text
fastapi-bookstore-postgres/
├── .env.example          # Sample environment variables
├── .gitignore            # Git exclusion rules
├── database.py           # Database connection and session engine
├── main.py               # FastAPI entry point & API route handlers
├── models.py             # SQLAlchemy database models
├── schemas.py            # Pydantic schemas for request/response validation
├── requirements.txt      # Project dependencies
└── README.md             # Project documentation

```

---

## ⚙️ Getting Started

### 1. Prerequisites

* Python 3.10+
* PostgreSQL server
* Git

### 2. Clone the Repository

```bash
git clone https://github.com/ahmadhooshmand1/fastapi-bookstore-postgres.git
cd fastapi-bookstore-postgres

```

### 3. Set Up Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate

```

### 4. Install Dependencies

```bash
pip install -r requirements.txt

```

### 5. Configure Environment Variables

Create a `.env` file from the example:

```bash
cp .env.example .env

```

Set your database connection string in `.env`:

```env
DATABASE_URL=postgresql://<DB_USER>:<DB_PASSWORD>@localhost:5432/<DB_NAME>

```

---

## ▶️ Running the Server

Start the server using Uvicorn:

```bash
uvicorn main:app --reload

```

The application runs at `[http://127.0.0.1:8000](http://127.0.0.1:8000)`.

---

## 📖 API Documentation

* **Swagger UI:** [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
* **ReDoc:** [http://127.0.0.1:8000/redoc](https://www.google.com/search?q=http://127.0.0.1:8000/redoc)

---

## 📌 API Endpoints

| HTTP Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/books` | Retrieve a list of all books |
| `GET` | `/books/{id}` | Retrieve details of a specific book by ID |
| `POST` | `/books` | Add a new book to the database |
| `PUT` | `/books/{id}` | Update an existing book's details |
| `DELETE` | `/books/{id}` | Remove a book from the database |

