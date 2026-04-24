---
name: nestjs-health-audit
description: Application Reliability and Health Monitoring
author: Diego Villanueva
trigger: When implementing health checks, readiness probes, or monitoring endpoints.
---

# NestJS Health & Reliability

Ensuring application uptime and monitoring using Terminus.

## ✅ ALWAYS
- Use `@nestjs/terminus` for implementing health check endpoints.
- Monitor critical dependencies: Database, Redis, Disk space, and Memory.
- Set up a standard `/health` endpoint for orchestrators (Kubernetes/Docker).
- Use `HttpHealthIndicator` to check external service availability.
- Log health check results for historical analysis.

## ❌ NEVER
- Expose detailed system health info without proper security or IP filtering.
- Block the main thread during health checks.
- Rely solely on a 200 OK response; check actual service functionality.

## 🛠 Patterns
- **Readiness Probe**: Determining if the app is ready to receive traffic.
- **Liveness Probe**: Determining if the app needs a restart.
