# 🚀 Semana 14 — ShipIt

> **Pipeline CI/CD completo con GitHub Actions, Docker y tests automáticos**

| Campo              | Detalle            |
| ------------------ | ------------------ |
| 📅 Fechas          | 6-7 de junio 2026  |
| 🏷️ Categoría       | DevOps & Cloud     |
| ⏱️ Tiempo estimado | 10-12 horas        |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio  |

---

## 🎯 Descripción

ShipIt es un pipeline CI/CD completo usando **GitHub Actions** que automatiza: linting, tests, build Docker, push a registry, y deploy. Toma uno de los proyectos anteriores (HotelAPI o GuestHub) y construye un pipeline profesional de integración y despliegue continuo.

---

## ✨ Features

### Pipeline CI
- [ ] Trigger en push y pull requests
- [ ] Job de linting (ESLint + Prettier check)
- [ ] Job de type checking (TypeScript --noEmit)
- [ ] Job de tests (Vitest con reporte de cobertura)
- [ ] Job de build Docker (multi-stage)
- [ ] Cache de node_modules
- [ ] Matrix testing (múltiples versiones Node.js)
- [ ] Badges de estado en README

### Pipeline CD
- [ ] Build y push de imagen Docker a GHCR
- [ ] Tags semánticos (latest, v1.0.0, sha)
- [ ] Deploy automático a staging
- [ ] Deploy manual a producción (workflow_dispatch)
- [ ] Rollback si health check falla

### Docker Avanzado
- [ ] Multi-stage Dockerfile optimizado
- [ ] Non-root user para seguridad
- [ ] Health check en container
- [ ] docker-compose para dev local

---

## 🛠️ Stack técnico

| Tecnología                    | Propósito        |
| ----------------------------- | ---------------- |
| **GitHub Actions**            | CI/CD            |
| **Docker**                    | Containerización |
| **GitHub Container Registry** | Image registry   |
| **Node.js + Express**         | App a desplegar  |
| **Vitest**                    | Tests            |
| **ESLint + Prettier**         | Linting          |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                        |
| -------------- | ------------------------------------------------ |
| 🌅 9:00-10:00  | Multi-stage Dockerfile optimizado                 |
| 🌅 10:00-12:00 | GitHub Actions: CI pipeline (lint, types, tests)  |
| 🌞 12:00-13:00 | Matrix testing + cache de dependencias            |
| 🌞 14:00-16:00 | CD pipeline: build + push Docker image            |
| 🌆 16:00-18:00 | Deploy automático + health check                  |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Conventional commits + releases        |
| 🌅 10:30-12:00 | Branch protection + PR templates       |
| 🌞 13:00-14:30 | Rollback + monitoring                  |
| 🌞 14:30-16:00 | Badges, documentación pipeline         |
| 🌆 16:00-17:00 | README con diagramas del pipeline      |

---

## ✅ Definición de "hecho"

- [ ] Pipeline CI corriendo en cada push/PR
- [ ] Tests, lint y type check automáticos
- [ ] Docker image en GHCR
- [ ] Deploy automático a staging
- [ ] Badges de CI en README
- [ ] Documentación del pipeline

---

## 💼 Lo que demuestra a Yuvod

| Habilidad  | Evidencia                           |
| ---------- | ----------------------------------- |
| CI/CD      | Pipeline completo GitHub Actions    |
| Docker     | Multi-stage, optimizado, seguro     |
| Git        | Conventional commits, protección    |
| DevOps     | Deploy automático, rollback         |
