# TP08 — Monitoreo con Prometheus y Grafana

## Stack completo
- **App Flask**: `:5000` (interno) - Expone `/metrics` con `prometheus_client`
- **Prometheus**: `:9090` - Scrape cada 15s, retención 15 días
- **Grafana**: `:3000` - Dashboards + provisioning automático
- **Node Exporter**: `:9100` (interno) - CPU, RAM, disco, red del host
- **cAdvisor**: `:8080` (interno) - Métricas de contenedores Docker

## Acceso y despliegue
```bash
docker compose up -d
