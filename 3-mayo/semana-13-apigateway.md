# 🚪 Semana 13 — APIGateway

> **Gateway centralizado con caché, autenticación, rate limiting y Express**

| Campo              | Detalle            |
| ------------------ | ------------------ |
| 📅 Fechas          | 30-31 de mayo 2026 |
| 🏷️ Categoría       | Full-Stack         |
| ⏱️ Tiempo estimado | 10-12 horas        |
| 📊 Dificultad      | ⭐⭐⭐⭐ Alto      |

---

## 🎯 Descripción

APIGateway es un gateway centralizado construido con Express que actúa como punto de entrada único para múltiples microservicios. Implementa autenticación JWT, rate limiting, caching con Redis, load balancing básico, y logging centralizado. Prepara la arquitectura para los microservicios del mes 4.

---

## ✨ Features

### Routing y proxy
- [ ] Reverse proxy hacia múltiples backends
- [ ] Enrutamiento basado en path prefix
- [ ] Versionado de API (/v1, /v2)
- [ ] Health checks de backends

### Seguridad
- [ ] Autenticación JWT centralizada
- [ ] Rate limiting por usuario/IP (express-rate-limit + Redis)
- [ ] CORS configurado por origen
- [ ] Protección contra ataques comunes (Helmet)

### Performance
- [ ] Caching de respuestas con Redis
- [ ] Cache invalidation configurable
- [ ] Compresión de respuestas (gzip)
- [ ] Request/Response logging

### Observabilidad
- [ ] Logging estructurado (Winston/Pino)
- [ ] Métricas de latencia por endpoint
- [ ] Dashboard de métricas del gateway
- [ ] Alertas de rate limit exceeded

---

## 🛠️ Stack técnico

| Tecnología              | Propósito           |
| ----------------------- | ------------------- |
| **Express.js**          | Framework           |
| **TypeScript**          | Tipado estricto     |
| **Redis**               | Cache + Rate limit  |
| **http-proxy-middleware**| Reverse proxy       |
| **JWT**                 | Autenticación       |
| **Helmet**              | Seguridad           |
| **Winston**             | Logging             |
| **Docker Compose**      | Infraestructura     |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Express + Redis + Docker                  |
| 🌅 10:00-12:00 | Reverse proxy + routing basado en paths          |
| 🌞 12:00-13:00 | Autenticación JWT centralizada                   |
| 🌞 14:00-16:00 | Rate limiting con Redis                          |
| 🌆 16:00-18:00 | Caching de respuestas + invalidation             |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Logging estructurado + métricas        |
| 🌅 10:30-12:00 | Health checks de backends              |
| 🌞 13:00-14:30 | Dashboard de métricas (React simple)   |
| 🌞 14:30-16:00 | Tests + seguridad                      |
| 🌆 16:00-17:00 | README y documentación                 |

---

## ✅ Definición de "hecho"

- [ ] Gateway proxy funcional hacia múltiples backends
- [ ] JWT auth centralizado
- [ ] Rate limiting con Redis
- [ ] Caching de respuestas
- [ ] Logging estructurado
- [ ] Docker Compose con todos los servicios
- [ ] Tests + README

---

## 💼 Valor para el portafolio

| Habilidad       | Evidencia                                   |
| --------------- | ------------------------------------------- |
| Arquitectura    | API Gateway como patrón de microservicios   |
| Node.js/Express | Middleware avanzado, proxy, streaming        |
| Redis           | Cache, rate limiting, session store          |
| Seguridad       | JWT, Helmet, CORS, rate limiting             |
| Escalabilidad   | Preparado para arquitectura distribuida      |
