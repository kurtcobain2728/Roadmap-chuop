# 🔀 Semana 15 — MicroServices

> **Arquitectura de microservicios con Node.js, Express, Docker y comunicación inter-servicio**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 13-14 de junio 2026 |
| 🏷️ Categoría       | DevOps & Cloud      |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐⭐ Alto       |

---

## 🎯 Descripción

MicroServices descompone una aplicación monolítica en **3 microservicios independientes** que se comunican entre sí: un servicio de usuarios, un servicio de contenido y un servicio de notificaciones. Cada uno tiene su propia base de datos MongoDB, su propio Dockerfile, y se comunican via HTTP y eventos.

En la industria se busca _"participar en el diseño de arquitecturas con microservicios"_.

---

## ✨ Features

### Microservicios
- [ ] **User Service**: auth, perfiles, roles (MongoDB propia)
- [ ] **Content Service**: canales, VOD, EPG (MongoDB propia)
- [ ] **Notification Service**: alerts, emails, push (MongoDB propia)

### Comunicación
- [ ] HTTP inter-servicio con retry y circuit breaker
- [ ] Service discovery básico con Docker DNS
- [ ] Shared events via HTTP webhooks
- [ ] Health checks entre servicios

### Infraestructura
- [ ] Docker Compose con todos los servicios
- [ ] Docker networks para aislamiento
- [ ] Nginx como reverse proxy / load balancer
- [ ] Logging centralizado
- [ ] Cada servicio con su propio package.json y Dockerfile

---

## 🛠️ Stack técnico

| Tecnología        | Propósito              |
| ----------------- | ---------------------- |
| **Node.js**       | Runtime                |
| **Express**       | Framework por servicio |
| **TypeScript**    | Tipado                 |
| **MongoDB**       | DB por servicio        |
| **Docker**        | Containerización       |
| **Nginx**         | Reverse proxy          |
| **Axios**         | HTTP inter-servicio    |

---

## 📁 Estructura del proyecto

```
microservices/
├── services/
│   ├── user-service/
│   │   ├── src/
│   │   ├── Dockerfile
│   │   ├── package.json
│   │   └── tsconfig.json
│   ├── content-service/
│   │   ├── src/
│   │   ├── Dockerfile
│   │   ├── package.json
│   │   └── tsconfig.json
│   └── notification-service/
│       ├── src/
│       ├── Dockerfile
│       ├── package.json
│       └── tsconfig.json
├── nginx/
│   └── nginx.conf
├── docker-compose.yml
├── Makefile
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                    |
| -------------- | -------------------------------------------- |
| 🌅 9:00-10:00  | Arquitectura: definir servicios y contratos   |
| 🌅 10:00-12:00 | User Service: auth, CRUD, MongoDB             |
| 🌞 12:00-13:00 | Content Service: canales, VOD básico           |
| 🌞 14:00-16:00 | Notification Service: alertas, webhooks        |
| 🌆 16:00-18:00 | Docker Compose + networking                    |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Comunicación HTTP inter-servicio       |
| 🌅 10:30-12:00 | Nginx reverse proxy + routing          |
| 🌞 13:00-14:30 | Health checks + retry + circuit breaker |
| 🌞 14:30-16:00 | Tests + logging centralizado           |
| 🌆 16:00-17:00 | README con diagrama de arquitectura    |

---

## ✅ Definición de "hecho"

- [ ] 3 microservicios funcionando independientemente
- [ ] Comunicación inter-servicio funcional
- [ ] Cada servicio con su propia MongoDB
- [ ] Docker Compose levanta todo
- [ ] Nginx como punto de entrada
- [ ] Tests por servicio
- [ ] README con diagrama de arquitectura

---

## 💼 Valor para el portafolio

| Habilidad        | Evidencia                                 |
| ---------------- | ----------------------------------------- |
| Microservicios   | 3 servicios desacoplados                  |
| Docker           | Multi-container, networking, compose      |
| Node.js/Express  | Múltiples servicios Express               |
| Arquitectura     | Service decomposition, inter-comunicación |
| Escalabilidad    | Cada servicio escala independientemente    |
