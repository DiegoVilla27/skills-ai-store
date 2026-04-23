---
description: 'Real-time Bidirectional Communication with WebSockets'
author: 'Diego Villanueva'
trigger: 'When implementing chat systems, real-time notifications, or live data updates.'
---

# NestJS WebSockets

Mastery of real-time communication using Gateways and Socket.io.

## ✅ ALWAYS
- Use `@WebSocketGateway()` to define your real-time entry points.
- Implement `OnGatewayInit`, `OnGatewayConnection`, and `OnGatewayDisconnect` for lifecycle management.
- Use `@SubscribeMessage()` to handle incoming events.
- Use `ValidationPipe` to validate data sent through sockets.
- Implement authentication using a custom `WsGuard`.

## ❌ NEVER
- Use WebSockets for standard request-response operations (use REST/GraphQL instead).
- Forget to handle connection errors and reconnections on the client side.
- Emit sensitive data to all connected clients; use "Rooms" for targeted broadcasting.

## 🛠 Patterns
- **Room Strategy**: Organizing clients into groups for efficient message delivery.
- **Ack Pattern**: Using acknowledgments to ensure the client received the event.
