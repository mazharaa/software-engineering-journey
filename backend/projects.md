# Backend Projects

Track roadmap.sh backend projects with recommended language choice between Go and Python.

---

## Language Selection Philosophy

- **Python** — best for beginner projects, data/text processing, API development, and rich ecosystem (FastAPI, Django, SQLAlchemy, Pillow, etc.)
- **Go** — best for networking, concurrency, performance-critical systems, real-time applications, and CLI tools that compile to single binaries

---

## Beginner (12 Projects)

| #   | Project                  | Type    | Recommended Language | Why                                                                                             |
| --- | ------------------------ | ------- | -------------------- | ----------------------------------------------------------------------------------------------- |
| 1   | Task Tracker             | CLI     | **Python**           | File I/O + JSON. Python's `json` and `argparse` make CLI trivial. Go requires more boilerplate. |
| 2   | GitHub User Activity     | CLI     | **Python**           | API calls + JSON parsing. Python's `requests` is simpler than Go's HTTP client for beginners.   |
| 3   | Expense Tracker          | CLI     | **Python**           | File storage + CRUD logic. Python's simplicity wins for learning fundamentals.                  |
| 4   | Number Guessing Game     | CLI     | **Python**           | Simple logic + random + loops. Python is more approachable for first projects.                  |
| 5   | Weather API              | API     | **Python**           | 3rd-party API + Redis caching. Python has `requests`, `redis-py`, FastAPI — very clean setup.   |
| 6   | Blogging Platform API    | API     | **Python**           | Basic CRUD + database. FastAPI/Flask makes REST APIs concise. Go needs more setup.              |
| 7   | Todo List API            | API     | **Python**           | Auth + CRUD + pagination. Python's JWT libs + SQLAlchemy are straightforward.                   |
| 8   | Expense Tracker API      | API     | **Python**           | JWT auth + filtering. FastAPI's dependency injection makes auth clean.                          |
| 9   | Server Performance Stats | CLI     | **Python**           | System metrics. Python's `psutil` is easier than parsing `/proc` in Go.                         |
| 10  | Log Archive Tool         | CLI     | **Python**           | File archiving + dates. Python's `shutil`, `datetime`, `pathlib` are beginner-friendly.         |
| 11  | Nginx Log Analyser       | CLI     | **Python**           | Log parsing. Python's string manipulation + regex is simpler for text processing.               |
| 12  | Unit Converter           | Web App | **Python**           | Simple conversion logic. Python's readability wins for learning.                                |

---

## Intermediate (9 Projects)

| #   | Project                     | Type   | Recommended Language | Why                                                                                                                       |
| --- | --------------------------- | ------ | -------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| 13  | Caching Proxy               | CLI    | **Go**               | HTTP proxy + caching + concurrency. Go's `net/http`, goroutines, and performance make it ideal.                           |
| 14  | Markdown Note-taking App    | API    | **Python**           | File uploads + markdown parsing + grammar check. Python's `markdown`, `language-tool-python` libs dominate.               |
| 15  | URL Shortening Service      | API    | **Go**               | High-throughput key lookups + redirects. Go's speed + Redis integration excels here.                                      |
| 16  | Broadcast Server            | CLI    | **Go**               | WebSockets + real-time broadcasting. Go's `gorilla/websocket` + goroutines are made for this.                             |
| 17  | Multi-Container Application | Docker | **Python**           | Project spec allows any language. Python + FastAPI + Docker is simpler for learning Docker concepts.                      |
| 18  | E-Commerce API              | API    | **Python**           | Complex domain + Stripe integration. Python's Django/Stripe SDK ecosystem is mature. Go is viable but requires more code. |
| 19  | Linux Server Setup          | Linux  | Bash (not Go/Python) | Pure sysadmin. Bash is the tool. If forced to choose: Python for Ansible automation.                                      |
| 20  | Workout Tracker             | API    | **Python**           | JWT + relational DB + seeding. FastAPI's auto-generated OpenAPI docs + SQLAlchemy win.                                    |
| 21  | Image Processing Service    | API    | **Python**           | Image transformations + S3 + queues. Python's `Pillow`, `boto3`, `celery` are industry standard.                          |

---

## Advanced (4 Projects)

| #   | Project                      | Type          | Recommended Language | Why                                                                                                                     |
| --- | ---------------------------- | ------------- | -------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| 22  | Movie Reservation System     | API           | **Go**               | Seat booking + concurrency + overbooking prevention. Go's transaction handling + goroutines are perfect.                |
| 23  | Real-time Leaderboard        | API           | **Go**               | Redis sorted sets + real-time updates + high frequency. Go's performance + Redis client are ideal.                      |
| 24  | Database Backup Utility      | CLI           | **Go**               | Multi-DB support + S3 + compression + cross-platform. Go compiles to single binary — perfect for CLI tools.             |
| 25  | Scalable E-Commerce Platform | Microservices | **Go**               | 6 microservices + API Gateway + Docker + CI/CD. Go is built for microservices: fast, small binaries, great concurrency. |

---

## Summary

| Level            | Python Wins | Go Wins |
| ---------------- | ----------: | ------: |
| Beginner (12)    |      **12** |       0 |
| Intermediate (9) |           5 |   **4** |
| Advanced (4)     |           0 |   **4** |
| **Total**        |      **17** |   **8** |

---

## Recommended Learning Path

1. Start all beginner projects with **Python** — focus on learning concepts, not fighting syntax.
2. Use **Go** for networking/concurrency intermediate projects (Caching Proxy, URL Shortener, Broadcast Server).
3. Complete all advanced projects with **Go** — this is where performance and concurrency matter most.

---

## Project Status Tracker

Track your progress below.

| Project                      | Repository                                           | Status  | Language Used | Notes |
| ---------------------------- | ---------------------------------------------------- | ------- | ------------- | ----- |
| Task Tracker                 | [Link](https://github.com/mazharaa/task-tracker-cli) | Done    | Python        |       |
| GitHub User Activity         |                                                      | Planned | Python        |       |
| Expense Tracker              |                                                      | Planned | Python        |       |
| Number Guessing Game         |                                                      | Planned | Python        |       |
| Weather API                  |                                                      | Planned | Python        |       |
| Blogging Platform API        |                                                      | Planned | Python        |       |
| Todo List API                |                                                      | Planned | Python        |       |
| Expense Tracker API          |                                                      | Planned | Python        |       |
| Server Performance Stats     |                                                      | Planned | Python        |       |
| Log Archive Tool             |                                                      | Planned | Python        |       |
| Nginx Log Analyser           |                                                      | Planned | Python        |       |
| Unit Converter               |                                                      | Planned | Python        |       |
| Caching Proxy                |                                                      | Planned | Go            |       |
| Markdown Note-taking App     |                                                      | Planned | Python        |       |
| URL Shortening Service       |                                                      | Planned | Go            |       |
| Broadcast Server             |                                                      | Planned | Go            |       |
| Multi-Container Application  |                                                      | Planned | Python        |       |
| E-Commerce API               |                                                      | Planned | Python        |       |
| Linux Server Setup           |                                                      | Planned | Bash          |       |
| Workout Tracker              |                                                      | Planned | Python        |       |
| Image Processing Service     |                                                      | Planned | Python        |       |
| Movie Reservation System     |                                                      | Planned | Go            |       |
| Real-time Leaderboard        |                                                      | Planned | Go            |       |
| Database Backup Utility      |                                                      | Planned | Go            |       |
| Scalable E-Commerce Platform |                                                      | Planned | Go            |       |

---

## Source

https://roadmap.sh/backend/projects
