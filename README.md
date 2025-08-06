# Fullstack Docker App

A simple full-stack app using **React (frontend)**, **Express (backend)**, and **PostgreSQL (database)** – all containerized using **Docker**.

---

## 📁 Project Structure

```
.
├── backend/              # Express server
│   └── index.js
├── frontend/             # React app
│   └── src/App.js
├── db/                   # SQL initialization
│   └── init.sql
├── .env                  # Environment variables
├── docker-compose.yml    # Multi-service config
└── README.md
```

---

## ⚙️ Tech Stack

* **Frontend**: React
* **Backend**: Node.js + Express
* **Database**: PostgreSQL
* **DevOps**: Docker, Docker Compose

---

## ✅ Features

* React fetches data from Express backend
* Express connects to PostgreSQL and serves an API
* PostgreSQL auto-initialized with sample SQL
* Fully dockerized with isolated containers

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone <repo-url>
cd project-folder
```

### 2. Create `.env` file

```env
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=your_db_name
DB_HOST=db
DB_PORT=5432
```

### 3. Run using Docker

```bash
docker-compose up --build
```

* Frontend: [http://localhost:3000](http://localhost:3000)
* Backend API: [http://localhost:5000/api](http://localhost:5000/api)
* PostgreSQL runs inside container on port 5432

---

## 📝 Notes

* If Docker warns about `version:` key, you can remove it from `docker-compose.yml`.
* Use `Docker Desktop` or `docker ps` to monitor containers.
* Make sure ports 3000, 5000, and 5432 are free.

---

## 📌 Example Flow

1. React (Frontend) makes a request to `/api`.
2. Express (Backend) handles the request, queries PostgreSQL.
3. Response is sent back and displayed in the browser.

---

## 📬 Author

Madhav Garg
[GitHub Profile](https://github.com/yourusername)
