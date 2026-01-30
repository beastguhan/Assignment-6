# Assignment-6
# 📊 Monitoring Stack with Prometheus + Grafana

This project demonstrates how to set up **local application monitoring** using **Prometheus** and **Grafana** with Docker Compose.

A sample Python application exposes a `/metrics` endpoint in Prometheus format, which is scraped by Prometheus and visualized using Grafana dashboards.

---

## 🎯 Objective

- Expose custom application metrics using Prometheus format
- Deploy Prometheus and Grafana locally using Docker Compose
- Collect and scrape metrics from a containerized app
- Visualize metrics using Grafana dashboards
- Export and store dashboards as JSON

---

## 🛠 Tech Stack

- Python (Flask)
- Prometheus
- Grafana
- Docker
- Docker Compose

---

---

## 🐍 Sample Application

The Python Flask application:
- Serves a basic HTTP endpoint
- Exposes metrics at `/metrics`
- Uses `prometheus_client` to track request count

### Exposed Metric

app_requests_total


---

## 🐳 Docker Compose Services

| Service | Description |
|------|------------|
| app | Python Flask app with /metrics endpoint |
| prometheus | Metrics collection and scraping |
| grafana | Metrics visualization |

---

## 🚀 Running the Monitoring Stack

Start all services:
```bash
docker compose up -d


Verify containers:

docker compose ps

Verification Steps
Application
curl http://localhost:5000

Metrics Endpoint
curl http://localhost:5000/metrics

  📈 Prometheus

Open Prometheus UI:

http://localhost:9090

Test query:

app_requests_total

📊 Grafana

Open Grafana UI:

http://localhost:3000



