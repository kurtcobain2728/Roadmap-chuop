# ☸️ Semana 17 — K8sDeploy

> **Despliegue y orquestación de microservicios con Kubernetes**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 27-28 de junio 2026 |
| 🏷️ Categoría       | DevOps & Cloud      |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐⭐ Alto       |

---

## 🎯 Descripción

K8sDeploy toma los microservicios de la semana 15 y los despliega en un cluster **Kubernetes** local (minikube o kind). Incluye Deployments, Services, Ingress, ConfigMaps, Secrets, HPA (autoscaling), y Helm charts. Demuestra conocimiento intermedio de K8s — competencia esencial para cualquier Full Stack Developer.

---

## ✨ Features

### Kubernetes Resources
- [ ] Deployments para cada microservicio
- [ ] Services (ClusterIP, NodePort)
- [ ] Ingress Controller con routing
- [ ] ConfigMaps para configuración
- [ ] Secrets para datos sensibles (DB passwords, JWT secret)
- [ ] PersistentVolumeClaims para MongoDB
- [ ] Namespaces para separación de ambientes

### Operaciones
- [ ] HPA (Horizontal Pod Autoscaler) basado en CPU
- [ ] Liveness y Readiness probes
- [ ] Rolling updates sin downtime
- [ ] Resource limits (CPU, memory)
- [ ] Pod disruption budgets

### Helm Charts
- [ ] Chart para cada microservicio
- [ ] values.yaml para configuración por ambiente
- [ ] Helm install/upgrade/rollback
- [ ] Templating de manifests

### Monitoring
- [ ] kubectl cheat sheet
- [ ] Dashboard de Kubernetes
- [ ] Logs centralizados con kubectl logs
- [ ] Port-forwarding para debug

---

## 🛠️ Stack técnico

| Tecnología       | Propósito                   |
| ---------------- | --------------------------- |
| **Kubernetes**   | Orquestación de contenedores |
| **minikube/kind**| Cluster local               |
| **kubectl**      | CLI de K8s                  |
| **Helm 3**       | Package manager de K8s      |
| **Docker**       | Images de los servicios     |
| **Nginx Ingress**| Ingress controller          |

---

## 📁 Estructura del proyecto

```
k8s-deploy/
├── k8s/
│   ├── namespaces/
│   │   └── hotel-system.yaml
│   ├── user-service/
│   │   ├── deployment.yaml
│   │   ├── service.yaml
│   │   ├── configmap.yaml
│   │   └── hpa.yaml
│   ├── content-service/
│   │   ├── deployment.yaml
│   │   ├── service.yaml
│   │   └── configmap.yaml
│   ├── notification-service/
│   │   ├── deployment.yaml
│   │   └── service.yaml
│   ├── mongodb/
│   │   ├── statefulset.yaml
│   │   ├── service.yaml
│   │   └── pvc.yaml
│   ├── rabbitmq/
│   │   ├── deployment.yaml
│   │   └── service.yaml
│   ├── ingress.yaml
│   └── secrets.yaml
├── helm/
│   └── hotel-platform/
│       ├── Chart.yaml
│       ├── values.yaml
│       ├── values-staging.yaml
│       ├── values-production.yaml
│       └── templates/
│           ├── deployment.yaml
│           ├── service.yaml
│           ├── ingress.yaml
│           └── _helpers.tpl
├── scripts/
│   ├── setup-cluster.sh
│   ├── deploy.sh
│   └── rollback.sh
├── Makefile
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                         |
| -------------- | ------------------------------------------------- |
| 🌅 9:00-10:00  | Setup: minikube/kind + kubectl                     |
| 🌅 10:00-12:00 | Deployments + Services para microservicios         |
| 🌞 12:00-13:00 | ConfigMaps + Secrets + MongoDB StatefulSet          |
| 🌞 14:00-16:00 | Ingress + routing + RabbitMQ en K8s                |
| 🌆 16:00-18:00 | Liveness/Readiness probes + resource limits        |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | HPA autoscaling + rolling updates      |
| 🌅 10:30-12:00 | Helm chart: templating + values        |
| 🌞 13:00-14:30 | Diferentes ambientes (staging/prod)    |
| 🌞 14:30-16:00 | Scripts de deploy/rollback             |
| 🌆 16:00-17:00 | README con comandos y diagrama         |

---

## ✅ Definición de "hecho"

- [ ] Todos los microservicios corriendo en K8s
- [ ] Ingress routing funcional
- [ ] ConfigMaps y Secrets en uso
- [ ] HPA configurado
- [ ] Helm chart instalable
- [ ] Liveness/Readiness probes
- [ ] README con guía de despliegue

---

## 💼 Valor para el portafolio

| Habilidad       | Evidencia                                  |
| --------------- | ------------------------------------------ |
| Kubernetes      | Deployments, Services, Ingress, HPA        |
| Helm            | Charts con values por ambiente             |
| Docker          | Images optimizadas para K8s               |
| Arquitectura    | Microservicios orquestados en K8s          |
| DevOps          | Deploy, rollback, autoscaling              |
| Nivel intermedio| Competencia esencial Full Stack          |
