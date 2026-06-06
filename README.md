# Datavyne AI Technologies — Official Website

A simple, modern company website built with **Node.js** and **Express**, served via **Docker**.

---

## Project Structure

```
datavyne-website/
├── src/
│   ├── server.js           # Express app entry point
│   ├── routes/
│   │   └── index.js        # Route handlers
│   └── public/             # Static frontend assets
│       ├── index.html      # Single-page website
│       ├── css/
│       │   └── style.css
│       └── js/
│           └── script.js
├── docker/
│   ├── Dockerfile          # Node.js 20 Alpine image
│   └── docker-compose.yml  # Service definition
├── .env.example            # Environment variable template
├── .gitignore
├── .dockerignore
└── package.json
```

---

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/) (Node.js is **not** required locally)

---

## Getting Started

**1. Clone the repository**

```bash
git clone https://github.com/codesteller/datavyne-website.git
cd datavyne-website
```

**2. Set up environment variables**

```bash
cp .env.example .env
```

**3. Build and start the container**

```bash
docker compose -f docker/docker-compose.yml up --build
```

The site will be available at **http://localhost:3000**

---

## Common Commands

| Action | Command |
|---|---|
| Start (with build) | `docker compose -f docker/docker-compose.yml up --build` |
| Start (background) | `docker compose -f docker/docker-compose.yml up -d` |
| Stop | `docker compose -f docker/docker-compose.yml down` |
| View logs | `docker compose -f docker/docker-compose.yml logs -f` |
| Rebuild image | `docker compose -f docker/docker-compose.yml build --no-cache` |

---

## Environment Variables

| Variable | Default | Description |
|---|---|---|
| `PORT` | `3000` | Port the server listens on |

---

## Tech Stack

- **Runtime:** Node.js 20 (Alpine)
- **Framework:** Express 4
- **Frontend:** Vanilla HTML / CSS / JavaScript
- **Container:** Docker + Docker Compose

---

## License

MIT © 2026 Datavyne AI Technologies
