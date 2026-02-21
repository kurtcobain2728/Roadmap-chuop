# 📡 Semana 10 — StreamManager

> **Gestor de streams/señales de TV con control en tiempo real (React + Node.js + WebSockets)**

| Campo              | Detalle          |
| ------------------ | ---------------- |
| 📅 Fechas          | 9-10 de mayo 2026|
| 🏷️ Categoría       | Full-Stack       |
| ⏱️ Tiempo estimado | 10-12 horas      |
| 📊 Dificultad      | ⭐⭐⭐⭐ Alto    |

---

## 🎯 Descripción

StreamManager es una aplicación full-stack para gestionar señales de TV/streams en tiempo real. Permite monitorear el estado de cada señal, iniciar/detener streams, ver métricas de calidad y recibir alertas cuando una señal falla. Usa WebSockets para comunicación bidireccional en tiempo real.

Core del negocio de Yuvod: _"simplificar la gestión de las señales"_.

---

## ✨ Features

### Frontend

- [ ] Dashboard con estado de todas las señales (activa, inactiva, error)
- [ ] Controles para iniciar/detener señales
- [ ] Métricas en tiempo real (bitrate, latencia, viewers)
- [ ] Alertas visuales cuando una señal falla
- [ ] Historial de eventos por señal
- [ ] Vista de mosaico con preview de canales

### Backend

- [ ] API REST para gestión de señales
- [ ] WebSocket server para eventos en tiempo real
- [ ] Simulador de métricas de stream
- [ ] Sistema de alertas con thresholds configurables
- [ ] Logging de eventos de señal

---

## 🛠️ Stack técnico

| Tecnología          | Propósito           |
| ------------------- | ------------------- |
| **React 18+**       | Frontend            |
| **Socket.io**       | WebSockets          |
| **Express.js**      | Backend + WS Server |
| **MongoDB**         | Base de datos       |
| **Chart.js**        | Gráficos            |
| **Material UI**     | Componentes UI      |
| **Docker Compose**  | Infraestructura     |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup proyecto + Docker Compose                  |
| 🌅 10:00-12:00 | Backend: modelos, API REST, WebSocket server     |
| 🌞 12:00-13:00 | Simulador de métricas de stream                  |
| 🌞 14:00-16:00 | Frontend: dashboard de señales + estado          |
| 🌆 16:00-18:00 | Controles de stream + WebSocket client           |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Gráficos de métricas en tiempo real    |
| 🌅 10:30-12:00 | Sistema de alertas                     |
| 🌞 13:00-14:30 | Historial de eventos + logs            |
| 🌞 14:30-16:00 | Tests + responsive                     |
| 🌆 16:00-17:00 | README y documentación                 |

---

## ✅ Definición de "hecho"

- [ ] Dashboard con estado de señales en tiempo real
- [ ] Controles funcionales start/stop de señales
- [ ] Métricas actualizándose via WebSocket
- [ ] Alertas cuando una señal falla
- [ ] Docker Compose funcional
- [ ] Tests básicos
- [ ] README con screenshots/GIFs

---

## 💼 Lo que demuestra a Yuvod

| Habilidad     | Evidencia                                       |
| ------------- | ----------------------------------------------- |
| Full-stack    | React + Express + MongoDB + WebSockets          |
| Tiempo real   | Socket.io para datos live                       |
| Dominio Yuvod | Gestión de señales TV — core del negocio        |
| React         | Estado reactivo, gráficos, controles            |
| Monitoreo     | Alertas, métricas, logs                         |
