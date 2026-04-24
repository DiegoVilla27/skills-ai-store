---
name: nestjs-queue-architect
description: Background Task Management with BullMQ
author: Diego Villanueva
trigger: When implementing background jobs, email sending, or heavy data processing.
---

# NestJS Queue Architect

Expert management of distributed background tasks using Redis and BullMQ.

## ✅ ALWAYS
- Use `@nestjs/bull` or `@nestjs/bullmq` for job queue integration.
- Define `Processors` and `Consumers` in separate modules.
- Handle job progress and completion events for UI feedback.
- Implement retries and exponential backoff for failed jobs.
- Use `Redis` as the backend for the queue.

## ❌ NEVER
- Perform heavy synchronous tasks inside the main request-response cycle.
- Forget to handle job failures; use "Dead Letter Queues" or logging.
- Store huge amounts of data in the job payload; store references (IDs) instead.

## 🛠 Patterns
- **Producer-Consumer**: Decoupling the task trigger from the execution.
- **Priority Queues**: Handling critical tasks (e.g., payments) before non-critical ones.
