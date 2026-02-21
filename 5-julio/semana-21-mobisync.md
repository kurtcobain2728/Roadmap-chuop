# 🔄 Semana 21 — MobiSync

> **App móvil con sincronización en tiempo real y modo offline (Flutter + WebSockets)**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 25-26 de julio 2026 |
| 🏷️ Categoría       | Flutter & Mobile    |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐⭐ Alto       |

---

## 🎯 Descripción

MobiSync es una app Flutter avanzada que implementa sincronización en tiempo real con WebSockets y funcionalidad offline-first. Permite que múltiples dispositivos se sincronicen instantáneamente (por ejemplo, cuando un huésped cambia de canal desde su teléfono, el panel del hotel se actualiza al instante).

---

## ✨ Features

### Tiempo real
- [ ] Conexión WebSocket persistente con Socket.io
- [ ] Sincronización de estado de TV entre dispositivos
- [ ] Notificaciones de eventos en tiempo real
- [ ] Indicador de conexión con auto-reconnect

### Offline first
- [ ] Almacenamiento local con SQLite/Drift
- [ ] Cola de acciones pendientes cuando offline
- [ ] Sincronización automática al reconectar
- [ ] Resolución de conflictos (last write wins)

### App
- [ ] Dashboard con estado actual del sistema
- [ ] Lista de dispositivos conectados
- [ ] Historial de acciones sincronizadas
- [ ] Configuración de preferencias

---

## 🛠️ Stack técnico

| Tecnología          | Propósito           |
| ------------------- | ------------------- |
| **Flutter 3+**      | Framework UI        |
| **Dart**            | Lenguaje            |
| **socket_io_client**| WebSockets          |
| **Drift (SQLite)**  | BD local            |
| **Riverpod**        | State management    |
| **Express + Socket.io** | Backend         |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup Flutter + backend Socket.io                |
| 🌅 10:00-12:00 | WebSocket client en Dart + eventos               |
| 🌞 12:00-13:00 | UI: dashboard con estado en tiempo real          |
| 🌞 14:00-16:00 | Almacenamiento local con Drift (SQLite)          |
| 🌆 16:00-18:00 | Cola de acciones offline                         |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Sincronización al reconectar           |
| 🌅 10:30-12:00 | Resolución de conflictos               |
| 🌞 13:00-14:30 | Historial de acciones + devices list   |
| 🌞 14:30-16:00 | Tests + polish                         |
| 🌆 16:00-17:00 | README con demo                        |

---

## ✅ Definición de "hecho"

- [ ] WebSocket sync funcionando en tiempo real
- [ ] Modo offline con cola de acciones
- [ ] Sincronización automática al reconectar
- [ ] UI responsive y pulida
- [ ] Tests básicos
- [ ] README con demo

---

## 💼 Lo que demuestra a Yuvod

| Habilidad         | Evidencia                                   |
| ----------------- | ------------------------------------------- |
| Flutter avanzado  | WebSockets, offline-first, sincronización   |
| Dart              | Patterns avanzados del lenguaje             |
| Tiempo real       | Socket.io en Flutter                        |
| Integración       | Flutter + Node.js backend                   |
| Arquitectura      | Offline-first con resolución de conflictos  |
