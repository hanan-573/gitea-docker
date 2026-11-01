# 🚀 Gitea Self-Hosted Server (Docker + Caddy)

A completely self-hosted, secure, and lightweight Git service (Gitea) running via Docker, with Caddy acting as a reverse proxy to handle automatic HTTPS/SSL certificates.

## 📌 Features

- **Gitea**: Lightweight code hosting alternative to GitHub.
- **Caddy Server**: Automatic HTTPS via Let's Encrypt/Cloudflare DNS.
- **Dockerized**: Easy to deploy, manage, and scale.
- **Secure**: Fully isolated containers with persistent data volumes.

## 🛠️ Prerequisites

Before you begin, ensure you have the following installed on your server:
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- A registered domain name pointing to your server's IP.

## 📂 Project Structure

```text
.
├── Caddyfile            # Caddy reverse proxy configuration
├── Dockerfile.caddy     # Custom Caddy image (with Cloudflare DNS plugin)
├── docker-compose.yml   # Main Docker services configuration
├── caddy-data/          # (Auto-generated) SSL certificates & Caddy data
├── gitea-data/          # (Auto-generated) Gitea repos, database & config
└── README.md            # Project documentation



🚀 Getting Started
1. Clone the repository
bash
git clone https://git.mughalkhan1.online/admin/gameverse.git
cd gameverse
2. Configure Environment
Ensure your docker-compose.yml has the correct domain and token values:

Set GITEA__server__DOMAIN to your domain.

Set CF_API_TOKEN to your Cloudflare API Token (if using DNS challenge).

3. Start the Services
bash
docker compose up -d
⚙️ Management Commands
Here are the essential commands to manage your Gitea server:

Start the project:

bash
docker compose up -d
Stop the project:

bash
docker compose down
Check the status:

bash
docker compose ps
View live logs (for debugging):

bash
docker compose logs -f
🔒 Access
Once the containers are running, access your Gitea instance at:
https://git.mughalkhan1.online:13004
