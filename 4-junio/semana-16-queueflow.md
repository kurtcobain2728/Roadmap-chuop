# 📨 Semana 16 — QueueFlow

> **Sistema de colas de mensajes con RabbitMQ, Node.js y Docker**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 20-21 de junio 2026 |
| 🏷️ Categoría       | DevOps & Cloud      |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐⭐ Alto       |

---

## 🎯 Descripción

QueueFlow implementa un sistema completo de **colas de mensajes con RabbitMQ** para procesamiento asíncrono. Incluye publishers, consumers, exchanges (direct, topic, fanout), dead letter queues, retry con backoff, y monitoreo. Directamente aplicable a cualquier arquitectura distribuida moderna.

Un Full Stack Developer profesional necesita _"experiencia con colas de mensajes (ej. RabbitMQ)"_.

---

## 🏗️ Arquitectura

```
┌──────────────┐     ┌──────────────┐     ┌──────────────────┐
│  Producer    │     │  RabbitMQ    │     │  Consumer        │
│  Service     │────▶│  Broker      │────▶│  Workers         │
│  (Express)   │     │              │     │                  │
└──────────────┘     │  Exchanges:  │     │  • Video Process │
                     │  ├─ direct   │     │  • Notification  │
┌──────────────┐     │  ├─ topic    │     │  • Analytics     │
│  API         │     │  └─ fanout   │     │  • Email         │
│  Gateway     │────▶│              │     │                  │
│              │     │  Queues:     │     └──────────────────┘
└──────────────┘     │  ├─ video    │              │
                     │  ├─ notify   │     ┌────────▼─────────┐
                     │  ├─ analytics│     │  Dead Letter     │
                     │  └─ email    │     │  Queue (DLQ)     │
                     └──────────────┘     └──────────────────┘
```

---

## ✨ Features

### RabbitMQ Patterns
- [ ] Direct exchange: routing 1:1 a queues específicas
- [ ] Topic exchange: routing por patrones (ej: `hotel.*.booking`)
- [ ] Fanout exchange: broadcast a múltiples consumers
- [ ] Dead Letter Queue: mensajes fallidos para reintento
- [ ] Message acknowledgment: at-least-once delivery
- [ ] Priority queues: mensajes urgentes primero

### Producers
- [ ] Servicio Express que publica eventos
- [ ] Eventos: nueva reserva, nuevo huésped, señal caída, etc.
- [ ] Serialización de mensajes con schema validation
- [ ] Retry de publicación si broker no disponible

### Consumers (Workers)
- [ ] Worker de procesamiento de video (simulado)
- [ ] Worker de notificaciones (email, push)
- [ ] Worker de analíticas (logging de eventos)
- [ ] Concurrency configurable por worker
- [ ] Graceful shutdown

### Monitoreo
- [ ] RabbitMQ Management UI incluida
- [ ] Métricas de mensajes procesados/fallidos
- [ ] Alertas cuando queue supera threshold
- [ ] Endpoint de health check del sistema

---

## 🛠️ Stack técnico

| Tecnología        | Propósito                      |
| ----------------- | ------------------------------ |
| **RabbitMQ**      | Message broker                 |
| **amqplib**       | Cliente AMQP para Node.js      |
| **Node.js**       | Runtime                        |
| **Express**       | API producer                   |
| **TypeScript**    | Tipado                         |
| **Docker Compose**| RabbitMQ + servicios           |
| **Vitest**        | Testing                        |

---

## 📁 Estructura del proyecto

```
queueflow/
├── producer/
│   ├── src/
│   │   ├── index.ts
│   │   ├── publishers/
│   │   │   ├── booking.publisher.ts
│   │   │   ├── signal.publisher.ts
│   │   │   └── guest.publisher.ts
│   │   └── config/
│   │       └── rabbitmq.ts
│   ├── Dockerfile
│   └── package.json
├── consumers/
│   ├── src/
│   │   ├── workers/
│   │   │   ├── video.worker.ts
│   │   │   ├── notification.worker.ts
│   │   │   ├── analytics.worker.ts
│   │   │   └── email.worker.ts
│   │   └── config/
│   │       └── rabbitmq.ts
│   ├── Dockerfile
│   └── package.json
├── shared/
│   ├── types/
│   │   └── events.ts
│   └── schemas/
│       └── message.schema.ts
├── docker-compose.yml
├── Makefile
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup: RabbitMQ en Docker + amqplib              |
| 🌅 10:00-12:00 | Direct exchange + primer producer/consumer       |
| 🌞 12:00-13:00 | Topic exchange + routing por patrones            |
| 🌞 14:00-16:00 | Múltiples workers + concurrency                  |
| 🌆 16:00-18:00 | Dead Letter Queue + retry con backoff            |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Fanout exchange + broadcast            |
| 🌅 10:30-12:00 | Message acknowledgment + priority      |
| 🌞 13:00-14:30 | API producer (Express) + endpoints     |
| 🌞 14:30-16:00 | Monitoreo + health checks + tests      |
| 🌆 16:00-17:00 | README con diagramas                   |

---

## ✅ Definición de "hecho"

- [ ] 3 tipos de exchange funcionando (direct, topic, fanout)
- [ ] Mínimo 4 workers consumers
- [ ] Dead Letter Queue con retry
- [ ] Message acknowledgment
- [ ] Docker Compose con RabbitMQ + servicios
- [ ] RabbitMQ Management UI accesible
- [ ] Tests + README con diagramas

---

## 💼 Valor para el portafolio

| Habilidad       | Evidencia                                    |
| --------------- | -------------------------------------------- |
| RabbitMQ        | Exchanges, queues, DLQ, acknowledgment       |
| Arquitectura    | Event-driven, pub/sub, workers               |
| Node.js         | Producers y consumers con amqplib            |
| Docker          | Multi-container con RabbitMQ                 |
| Escalabilidad   | Workers horizontalmente escalables           |
| Resiliencia     | DLQ, retry, graceful shutdown                |
