# Grafana-Loki-Promtail

Start command:

```bash
docker compose up
```

## Grafana

Run on: http://localhost:3000

## Loki

Run on: http://localhost:3100/metrics

## Promtail

Example how to scrape log location:

```yaml
scrape_configs:
  - job_name: mongodb
    static_configs:
      - targets:
          - localhost
        labels:
          job: mongodb
          __path__: /var/log/*.log
```
