# YBO Central Monitoring System

Port-based monitoring architecture for YBO services.

## Quick Start

```bash
cd Ybo.Monitor
docker-compose up -d
```

## Access Points

- **Grafana**: http://localhost:3000 (admin/ybo-admin-2024)
- **Prometheus**: http://localhost:9090
- **Alertmanager**: http://localhost:9093

## Architecture

Each YBO service exposes metrics on host ports:
- YBO API: :5001/metrics
- YBO CDN: :5002/metrics
- YBO Video: :8765/metrics
- PostgreSQL: :9187
- Redis: :9121

## Port Plan

| Service | Port |
|---------|------|
| Grafana | 3000 |
| Prometheus | 9090 |
| Alertmanager | 9093 |
| Node Exporter | 9100 |
| cAdvisor | 8082 |

## Services Setup

Each service must expose metrics endpoint on designated port.