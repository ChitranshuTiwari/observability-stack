# Observability Stack

> A hands-on DevOps portfolio project demonstrating monitoring and observability with Prometheus, Grafana, and Alertmanager. Built for learning and GSoC preparation.

Prometheus + Grafana + Alertmanager + sample app with custom metrics.

## Architecture

```
┌─────────────┐     ┌────────────┐     ┌────────────┐
│ Sample App  │────▶│ Prometheus │────▶│  Grafana   │
│  :8080     │     │   :9090    │     │   :3000    │
└─────────────┘     └─────┬──────┘     └────────────┘
                         │
                         ▼
┌─────────────────────────────────┐
│         Alertmanager :9093      │
└─────────────────────────────────┘
```

## Quick Start

```bash
docker compose up -d
```

- **Grafana:** http://localhost:3000 (admin/admin)
- **Prometheus:** http://localhost:9090
- **Sample App:** http://localhost:8080
- **Metrics:** http://localhost:8080/metrics

## License

MIT
