# Prometheus & Grafana Monitoring Stack

Monitoring stack with Prometheus and Grafana, preconfigured for TS/Node.js application metrics.

## Prerequisites
- Docker
- Docker Compose

## Directory Structure
```
.
├── README.md
├── docker-compose.yml
├── prometheus/
│   └── prometheus.yml
└── grafana/
    └── provisioning/
        ├── dashboards/
        │   ├── nodejs.json
        │   └── default.yaml
        └── datasources/
```

## Quick Start
1. Create the directory structure
2. Place configuration files in their respective directories
3. Start the stack:
   ```bash
   docker-compose up -d
   ```

## Access
- Prometheus: http://localhost:9090
- Grafana: http://localhost:3000
  - Username: admin
  - Password: admin

## Metrics
The stack is configured to scrape:
- Prometheus itself (localhost:9090)
- CoZero API (api.cozero.io/v1/metrics)

## Dashboard
Includes a preconfigured dashboard with:
- Event Loop Lag
- Heap Usage
- Prisma Query Statistics
- HTTP Request Rates

## Maintenance
To update configurations:
1. Modify the relevant files
2. Restart the services:
   ```bash
   docker-compose restart
   ```