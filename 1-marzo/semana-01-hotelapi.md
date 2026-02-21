# 🏨 Semana 01 — HotelAPI

> **API REST completa para gestión hotelera con Node.js, Express, MongoDB y TypeScript**

| Campo              | Detalle              |
| ------------------ | -------------------- |
| 📅 Fechas          | 7-8 de marzo 2026    |
| 🏷️ Categoría       | Backend Foundations  |
| ⏱️ Tiempo estimado | 10-12 horas          |
| 📊 Dificultad      | ⭐⭐ Intermedio-bajo |

---

## 🎯 Descripción

HotelAPI es una API REST profesional para gestión de habitaciones, huéspedes y servicios de un hotel. Es el primer proyecto del portafolio y establece las bases del stack backend: **Node.js + Express + MongoDB + TypeScript**. Incluye CRUD completo, filtros avanzados, paginación, validación robusta con Zod y documentación automática con Swagger.

Simula un contexto real del sector hotelero — un dominio real y frecuente en la industria.

---

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────┐
│              Cliente (HTTP)              │
└──────────────────┬──────────────────────┘
                   │
          ┌────────▼────────┐
          │   Express App   │
          │  (Routers +     │
          │   Middleware)    │
          └────────┬────────┘
                   │
          ┌────────▼────────┐
          │  Service Layer  │
          │ (Business Logic)│
          └────────┬────────┘
                   │
          ┌────────▼────────┐
          │   Mongoose ODM   │
          │   (Data Layer)   │
          └────────┬────────┘
                   │
          ┌────────▼────────┐
          │    MongoDB       │
          │    (Docker)      │
          └─────────────────┘
```

---

## ✨ Features

### Core

- [ ] CRUD completo de habitaciones (tipos, precios, disponibilidad)
- [ ] CRUD de huéspedes (datos personales, historial)
- [ ] Gestión de reservas (check-in, check-out, estados)
- [ ] Relación huésped → reserva → habitación
- [ ] Estados de habitación (disponible, ocupada, mantenimiento, limpieza)

### Avanzado

- [ ] Filtros por tipo, precio, disponibilidad, fechas
- [ ] Paginación con cursor o offset
- [ ] Ordenamiento por múltiples campos
- [ ] Búsqueda por texto en nombre y descripción
- [ ] Validación robusta con Zod
- [ ] Manejo de errores centralizado y consistente

### Infraestructura

- [ ] Docker Compose (app + MongoDB)
- [ ] Tests con Vitest + Supertest (cobertura ≥ 80%)
- [ ] Documentación Swagger automática (swagger-jsdoc)
- [ ] Variables de entorno tipadas con Zod
- [ ] ESLint + Prettier configurados
- [ ] TypeScript estricto (sin `any`)

---

## 🛠️ Stack técnico

| Tecnología          | Propósito                  |
| ------------------- | -------------------------- |
| **Node.js 20+**     | Runtime                    |
| **Express.js**      | Framework web              |
| **TypeScript 5+**   | Tipado estricto            |
| **MongoDB**         | Base de datos NoSQL        |
| **Mongoose**        | ODM para MongoDB           |
| **Zod**             | Validación de schemas      |
| **Docker Compose**  | Infraestructura local      |
| **Vitest**          | Testing                    |
| **Supertest**       | Testing HTTP               |
| **swagger-jsdoc**   | Documentación API          |

---

## 📁 Estructura del proyecto

```
hotelapi/
├── src/
│   ├── index.ts               # Entry point
│   ├── app.ts                 # Express app setup
│   ├── config/
│   │   └── env.ts             # Variables de entorno tipadas (Zod)
│   ├── models/
│   │   ├── room.model.ts      # Mongoose schema de habitaciones
│   │   ├── guest.model.ts     # Mongoose schema de huéspedes
│   │   └── booking.model.ts   # Mongoose schema de reservas
│   ├── routes/
│   │   ├── room.routes.ts     # Endpoints de habitaciones
│   │   ├── guest.routes.ts    # Endpoints de huéspedes
│   │   └── booking.routes.ts  # Endpoints de reservas
│   ├── controllers/
│   │   ├── room.controller.ts
│   │   ├── guest.controller.ts
│   │   └── booking.controller.ts
│   ├── services/
│   │   ├── room.service.ts    # Lógica de negocio
│   │   ├── guest.service.ts
│   │   └── booking.service.ts
│   ├── middleware/
│   │   ├── errorHandler.ts    # Manejo centralizado de errores
│   │   ├── validator.ts       # Middleware de validación Zod
│   │   └── logger.ts          # Logging estructurado
│   ├── schemas/
│   │   ├── room.schema.ts     # Zod schemas
│   │   ├── guest.schema.ts
│   │   └── booking.schema.ts
│   └── utils/
│       ├── pagination.ts      # Helpers de paginación
│       └── database.ts        # Conexión MongoDB
├── tests/
│   ├── room.test.ts
│   ├── guest.test.ts
│   └── booking.test.ts
├── docker-compose.yml
├── Dockerfile
├── tsconfig.json
├── package.json
├── Makefile
├── .env.example
└── README.md
```

---

## 📡 Endpoints de la API

```
GET    /api/v1/rooms              # Listar habitaciones (con filtros y paginación)
POST   /api/v1/rooms              # Crear habitación
GET    /api/v1/rooms/:id          # Obtener habitación por ID
PUT    /api/v1/rooms/:id          # Actualizar habitación
DELETE /api/v1/rooms/:id          # Eliminar habitación

GET    /api/v1/guests             # Listar huéspedes
POST   /api/v1/guests             # Crear huésped
GET    /api/v1/guests/:id         # Obtener huésped con historial
PUT    /api/v1/guests/:id         # Actualizar huésped
DELETE /api/v1/guests/:id         # Eliminar huésped

GET    /api/v1/bookings           # Listar reservas
POST   /api/v1/bookings           # Crear reserva
GET    /api/v1/bookings/:id       # Obtener reserva
PUT    /api/v1/bookings/:id       # Actualizar reserva (check-in/out)
DELETE /api/v1/bookings/:id       # Cancelar reserva

GET    /api/v1/health             # Health check
GET    /api-docs                  # Documentación Swagger
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                            |
| -------------- | ---------------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Node.js, TypeScript, Express, Docker Compose  |
| 🌅 10:00-11:00 | Modelos Mongoose + conexión MongoDB                  |
| 🌞 11:00-13:00 | Schemas Zod + Service layer                          |
| 🌞 14:00-17:00 | Controllers + Routes: CRUD de rooms, guests, bookings|
| 🌆 17:00-18:00 | Filtros, paginación y búsqueda                       |

### Domingo

| Hora           | Actividad                            |
| -------------- | ------------------------------------ |
| 🌅 9:00-11:00  | Tests con Vitest + Supertest         |
| 🌅 11:00-12:00 | Manejo de errores centralizado       |
| 🌞 13:00-14:00 | Polish: validaciones y edge cases    |
| 🌞 14:00-16:00 | Swagger docs, README, Makefile       |
| 🌆 16:00-17:00 | Review final, CI básico y push       |

---

## ✅ Definición de "hecho"

- [ ] API funcional con todos los endpoints
- [ ] Docker Compose levanta todo con un solo comando
- [ ] Tests pasan con cobertura ≥ 80%
- [ ] Documentación Swagger generada automáticamente
- [ ] README con instrucciones de setup y uso
- [ ] TypeScript estricto (sin `any`)
- [ ] ESLint + Prettier sin errores
- [ ] Repositorio en GitHub con CI básico

---

## 💼 Valor para el portafolio

| Habilidad          | Evidencia                                |
| ------------------ | ---------------------------------------- |
| Node.js + Express  | API RESTful profesional con TypeScript   |
| MongoDB            | Mongoose schemas, relaciones, queries    |
| TypeScript         | Tipado estricto en todo el proyecto      |
| Sector hotelero    | Dominio del negocio (rooms, guests, etc) |
| Testing            | Vitest + Supertest con buena cobertura   |
| Docker             | Docker Compose, containerización         |
| Clean Code         | Arquitectura en capas, SOLID             |
