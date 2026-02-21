# 🔐 Semana 02 — AuthNode

> **Sistema de autenticación y autorización completo con Express, JWT y MongoDB**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 14-15 de marzo 2026 |
| 🏷️ Categoría       | Backend Foundations |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

AuthNode es un sistema de autenticación y autorización listo para producción construido con Express y MongoDB. Va más allá del login básico: implementa JWT con refresh tokens, roles y permisos granulares (RBAC), registro seguro, y endpoints protegidos. Este módulo se reutilizará como base de autenticación en todos los proyectos futuros.

Directamente aplicable a Yuvod donde se necesita gestionar diferentes perfiles de acceso (huéspedes, staff del hotel, administradores de la plataforma).

---

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────┐
│              Cliente (HTTP)              │
└──────────────────┬──────────────────────┘
                   │
          ┌────────▼────────┐
          │  Express + TS   │
          │  (Routes +      │
          │   Middleware)    │
          └────────┬────────┘
                   │
     ┌─────────────┼─────────────┐
     │             │             │
┌────▼────┐  ┌────▼────┐  ┌────▼────┐
│  Auth   │  │  Users  │  │  Roles  │
│ Module  │  │ Module  │  │ Module  │
│ (JWT)   │  │ (CRUD)  │  │ (RBAC)  │
└────┬────┘  └────┬────┘  └────┬────┘
     │             │             │
     └─────────────┼─────────────┘
                   │
          ┌────────▼────────┐
          │    MongoDB       │
          │    (Docker)      │
          └─────────────────┘
```

---

## ✨ Features

### Autenticación

- [ ] Registro de usuarios con validación robusta
- [ ] Login con JWT (access token + refresh token)
- [ ] Refresh token rotation (seguridad)
- [ ] Logout con blacklist de tokens (Redis o MongoDB)
- [ ] Cambio de contraseña
- [ ] Reset de contraseña (flujo con token temporal)

### Autorización (RBAC)

- [ ] Roles predefinidos: `admin`, `hotel_manager`, `staff`, `guest`
- [ ] Permisos granulares por recurso y acción
- [ ] Middleware de autenticación reutilizable
- [ ] Middleware de autorización por rol
- [ ] Guards personalizados por endpoint

### Gestión de usuarios

- [ ] CRUD de usuarios (solo admin)
- [ ] Perfil de usuario (lectura/edición propia)
- [ ] Listado con filtros y paginación
- [ ] Soft delete de usuarios
- [ ] Auditoría de último login

### Seguridad

- [ ] Rate limiting en endpoints de auth (express-rate-limit)
- [ ] Password hashing con bcrypt
- [ ] Validación de fortaleza de contraseña
- [ ] Protección contra brute force
- [ ] Helmet para headers de seguridad
- [ ] CORS configurado correctamente

---

## 🛠️ Stack técnico

| Tecnología              | Propósito             |
| ----------------------- | --------------------- |
| **Express.js**          | Framework web         |
| **TypeScript**          | Tipado estricto       |
| **jsonwebtoken**        | Generación de JWT     |
| **bcrypt**              | Hashing de passwords  |
| **MongoDB + Mongoose**  | Base de datos         |
| **Zod**                 | Validación            |
| **Helmet**              | Headers de seguridad  |
| **express-rate-limit**  | Rate limiting         |
| **Docker Compose**      | Infraestructura local |
| **Vitest + Supertest**  | Testing               |
| **swagger-jsdoc**       | Documentación API     |

---

## 📡 Endpoints de la API

```
POST   /api/v1/auth/register         # Registro de usuario
POST   /api/v1/auth/login             # Login → access + refresh token
POST   /api/v1/auth/refresh           # Refrescar access token
POST   /api/v1/auth/logout            # Logout (invalidar token)
POST   /api/v1/auth/change-password   # Cambiar contraseña
POST   /api/v1/auth/forgot-password   # Solicitar reset de password
POST   /api/v1/auth/reset-password    # Confirmar reset con token

GET    /api/v1/users/me               # Mi perfil
PUT    /api/v1/users/me               # Editar mi perfil
GET    /api/v1/users                  # Listar usuarios (admin)
GET    /api/v1/users/:id              # Ver usuario (admin)
PUT    /api/v1/users/:id/role         # Asignar rol (admin)
DELETE /api/v1/users/:id              # Eliminar usuario (admin)
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Express, TypeScript, Docker Compose       |
| 🌅 10:00-11:30 | Modelo de usuario con Mongoose + validación Zod  |
| 🌞 11:30-13:00 | Registro y login con JWT + bcrypt                |
| 🌞 14:00-16:00 | Refresh tokens, logout, cambio de password       |
| 🌆 16:00-18:00 | Sistema de roles y permisos (RBAC middleware)    |

### Domingo

| Hora           | Actividad                           |
| -------------- | ----------------------------------- |
| 🌅 9:00-11:00  | CRUD de usuarios + perfil           |
| 🌅 11:00-12:30 | Tests de autenticación y permisos   |
| 🌞 13:30-15:00 | Rate limiting, Helmet, seguridad    |
| 🌞 15:00-16:30 | Documentación API (Swagger)         |
| 🌆 16:30-17:30 | README y push a GitHub              |

---

## ✅ Definición de "hecho"

- [ ] Flujo completo de autenticación funcional
- [ ] RBAC con al menos 4 roles (admin, hotel_manager, staff, guest)
- [ ] Tests de cada endpoint de auth con Vitest + Supertest
- [ ] Rate limiting configurado en endpoints sensibles
- [ ] Documentación Swagger completa
- [ ] Docker Compose funcional
- [ ] TypeScript estricto
- [ ] README con instrucciones y ejemplos de uso

---

## 💼 Lo que demuestra a Yuvod

| Habilidad    | Evidencia                                        |
| ------------ | ------------------------------------------------ |
| Node.js/Express | API REST con middleware avanzado               |
| Seguridad    | JWT, RBAC, rate limiting, bcrypt, Helmet         |
| MongoDB      | Modelos de usuario con Mongoose, queries         |
| TypeScript   | Interfaces tipadas para auth y usuarios          |
| Arquitectura | Middleware reutilizable, separación de concerns   |
| Testing      | Flujos de auth complejos testeados               |
| Dominio hotel| Roles específicos del sector hotelero            |
