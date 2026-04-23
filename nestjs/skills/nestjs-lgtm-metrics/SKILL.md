---
description: 'Full-stack Observability with Prometheus and Grafana'
author: 'Diego Villanueva'
trigger: 'When implementing metrics, logging, and performance monitoring.'
---

# NestJS Observability (LGTM)

Monitoring application performance and health using the LGTM stack.

## ✅ ALWAYS
- Use `@willsoto/nestjs-prometheus` for exposing metrics.
- Track standard metrics: Request count, duration, and error rate (RED pattern).
- Use `Winston` or `Pino` for structured logging that Loki can ingest.
- Implement **Tracing** using OpenTelemetry to visualize request flows.
- Export metrics to a `/metrics` endpoint for Prometheus scraping.

## ❌ NEVER
- Log sensitive data (passwords, PII) to your observability stack.
- Overload the app with too many custom metrics that impact performance.
- Ignore performance spikes; set up alerts in Grafana.

## 🛠 Patterns
- **Histogram Metrics**: Measuring the latency distribution of API calls.
- **Trace Context**: Passing the trace ID between microservices.
