# holbertonschool-softy-pinko-docker
# Softy Pinko Docker Project

A dockerized web application infrastructure using Nginx as a reverse proxy and load balancer.

## Project Structure

- **task0** - Basic Docker image based on Ubuntu that prints "Hello, World!"
- **task1** - Docker image with a Flask API server
- **task2** - Docker image with a static Nginx front-end server
- **task3** - Combined front-end and back-end in separate Docker containers
- **task4** - Docker Compose to manage front-end and back-end services together
- **task5** - Added Nginx reverse proxy to route traffic between front-end and back-end
- **task6** - Added load balancing with Round Robin algorithm across 2 API servers

## Architecture
Client → Proxy (port 80) → Front-end (port 9000)
→ Back-end 1 (port 5252)
→ Back-end 2 (port 5252)

## How to Run

```bash
cd task6
docker-compose build
docker-compose up --scale back-end=2
```

Then open: `http://localhost:80`
