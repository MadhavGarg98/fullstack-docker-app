# Fullstack Docker App

# 🚀 Fullstack Docker App – Mini Project 2

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
# 🚀 Fullstack Docker App – Mini Project 3

This project is a **Dockerized full-stack application** with persistent PostgreSQL storage. It showcases how to use Docker volumes for data persistence and Docker commands for debugging and container management.

---

## 📦 Tech Stack

- **Frontend**: React (or your choice)
- **Backend**: Node.js / Express
- **Database**: PostgreSQL 13
- **Containerization**: Docker & Docker Compose

---

## 🧠 Features Implemented

- ✅ Docker Compose setup for full stack (frontend + backend + database)
- ✅ Persistent database using named volume (`db-data`)
- ✅ Docker debugging using `logs`, `exec`, and `ps`
- ✅ Verified data remains intact after container restart

---

## 📁 Project Structure

```
fullstack-docker-app/
│
├── frontend/                # Frontend source code (with Dockerfile)
├── backend/                 # Backend source code (with Dockerfile)
├── docker-compose.yml       # Multi-container setup
├── .env                     # Environment variables for DB
├── README.md                # You're reading it!
└── db-data/ (auto-generated) # Docker volume for PostgreSQL (not pushed to repo)
```

---

## ⚙️ Environment Setup

Create a `.env` file at the root with:

```env
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=your_db_name
```

---

## 🚀 Run the Application

Make sure Docker is running. Then:

```bash
docker-compose up --build
```

Visit your app:

- Frontend → `http://localhost:3000`
- Backend → `http://localhost:5000` (if applicable)

---

## 💾 Volume Persistence (PostgreSQL)

We're using a named volume:
```yaml
volumes:
  db-data:
```

Mapped to Postgres data folder:
```yaml
services:
  db:
    ...
    volumes:
      - db-data:/var/lib/postgresql/data
```

This ensures that **data is not lost** even after:
```bash
docker-compose down
```

---

## 🐳 Docker Commands Used

### Check container status:
```bash
docker ps
```

### View logs:
```bash
docker logs fullstack-docker-app-backend-1
```

### Enter running container:
```bash
docker exec -it fullstack-docker-app-backend-1 sh
```

### Stop and start without removing:
```bash
docker-compose stop
docker-compose start
```

---

## ✅ How to Verify Persistence

1. Run the app and add some data via the frontend or backend
2. Stop and start containers:
   ```bash
   docker-compose stop
   docker-compose start
   ```
3. Refresh the browser – **data should still be there!**



## 🔗 GitHub Submission

> Make sure your repo is public and includes:
- frontend/
- backend/
- Dockerfiles
- docker-compose.yml
- .env (sample)
- README.md

---

## 🧑‍💻 Author

Madhav Garg
[GitHub Profile](https://github.com/yourusername)


