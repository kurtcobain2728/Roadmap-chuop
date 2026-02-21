# ⚙️ Semana 18 — CICDPipeline

> **Pipeline avanzado de integración/despliegue continuo con testing, Docker y K8s**

| Campo              | Detalle           |
| ------------------ | ----------------- |
| 📅 Fechas          | 4-5 de julio 2026 |
| 🏷️ Categoría       | DevOps & Cloud    |
| ⏱️ Tiempo estimado | 10-12 horas       |
| 📊 Dificultad      | ⭐⭐⭐⭐ Alto     |

---

## 🎯 Descripción

CICDPipeline es un pipeline CI/CD avanzado que integra todo lo aprendido: testing automatizado, linting, build Docker, push a registry, deploy a Kubernetes, y rollback automático. Es la culminación de todo el mes de DevOps.

---

## ✨ Features

### Pipeline completo
- [ ] Multi-stage pipeline (test → build → deploy)
- [ ] Tests en CI con reportes de cobertura
- [ ] Build Docker multi-arch (amd64 + arm64)
- [ ] Push a container registry con tagging semántico
- [ ] Deploy a K8s con Helm upgrade
- [ ] Smoke tests post-deploy
- [ ] Rollback automático si falla

### Ambientes
- [ ] Dev: deploy en cada push a feature branch
- [ ] Staging: deploy automático en merge a develop
- [ ] Production: deploy manual con approval
- [ ] Preview environments para PRs

### Seguridad
- [ ] Scanning de vulnerabilidades (Trivy)
- [ ] SAST (análisis de código estático)
- [ ] Secrets management con GitHub Secrets
- [ ] Signed Docker images

---

## 🛠️ Stack técnico

| Tecnología        | Propósito         |
| ----------------- | ----------------- |
| **GitHub Actions** | CI/CD            |
| **Docker**        | Containerización  |
| **Kubernetes**    | Deploy target     |
| **Helm**          | K8s deployments   |
| **Trivy**         | Vulnerability scan|
| **Vitest**        | Tests             |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                    |
| -------------- | -------------------------------------------- |
| 🌅 9:00-10:00  | Diseño del pipeline multi-stage               |
| 🌅 10:00-12:00 | CI: tests + lint + type check + cobertura     |
| 🌞 12:00-13:00 | Build Docker multi-arch + push                |
| 🌞 14:00-16:00 | Deploy a K8s con Helm upgrade                 |
| 🌆 16:00-18:00 | Smoke tests post-deploy + rollback            |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Preview environments para PRs          |
| 🌅 10:30-12:00 | Vulnerability scanning (Trivy)         |
| 🌞 13:00-14:30 | Multiple ambientes (dev/staging/prod)  |
| 🌞 14:30-16:00 | Documentación completa del pipeline    |
| 🌆 16:00-17:00 | README con diagramas del flujo         |

---

## ✅ Definición de "hecho"

- [ ] Pipeline corriendo end-to-end
- [ ] Tests + linting en CI
- [ ] Deploy automático a K8s
- [ ] Rollback automático funcional
- [ ] Vulnerability scanning
- [ ] Al menos 2 ambientes configurados
- [ ] README con diagrama del pipeline

---

## 💼 Valor para el portafolio

| Habilidad  | Evidencia                                   |
| ---------- | ------------------------------------------- |
| CI/CD      | Pipeline completo production-ready          |
| DevOps     | Integración de todo el stack DevOps         |
| K8s        | Deploy automatizado a Kubernetes            |
| Seguridad  | Vulnerability scanning, signed images       |
| Madurez    | Pipeline profesional de empresa             |
