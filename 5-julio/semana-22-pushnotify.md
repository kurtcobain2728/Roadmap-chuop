# 🔔 Semana 22 — PushNotify

> **Sistema de notificaciones push multiplataforma con Flutter, Firebase y Express**

| Campo              | Detalle            |
| ------------------ | ------------------ |
| 📅 Fechas          | 1-2 de agosto 2026 |
| 🏷️ Categoría       | Flutter & Mobile   |
| ⏱️ Tiempo estimado | 10-12 horas        |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio  |

---

## 🎯 Descripción

PushNotify implementa un sistema completo de notificaciones push para una app hotelera: notificaciones de servicio, alertas del hotel, promociones y recordatorios. Usa **Firebase Cloud Messaging** en el cliente Flutter y un backend Express que envía notificaciones a dispositivos específicos o a todos los huéspedes.

---

## ✨ Features

### Notificaciones
- [ ] Push notifications via Firebase Cloud Messaging
- [ ] Notificaciones a dispositivo específico (por token)
- [ ] Notificaciones a todos los huéspedes de un hotel (topic)
- [ ] Notificaciones con datos (deep linking)
- [ ] Notificaciones programadas (ej: checkout reminder)

### Backend
- [ ] API para enviar notificaciones (Express)
- [ ] Gestión de tokens de dispositivos en MongoDB
- [ ] Templates de notificaciones predefinidas
- [ ] Historial de notificaciones enviadas
- [ ] Segmentación por hotel

### App Flutter
- [ ] Recepción de notificaciones foreground/background
- [ ] Centro de notificaciones con historial
- [ ] Deep linking a pantalla específica
- [ ] Badges y contadores de no leídas
- [ ] Preferencias de notificación

---

## 🛠️ Stack técnico

| Tecnología              | Propósito              |
| ----------------------- | ---------------------- |
| **Flutter 3+**          | App móvil              |
| **Firebase Messaging**  | Push notifications     |
| **firebase_messaging**  | Plugin Flutter         |
| **Express.js**          | Backend                |
| **firebase-admin**      | SDK servidor Firebase  |
| **MongoDB**             | Almacenamiento         |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                        |
| -------------- | ------------------------------------------------ |
| 🌅 9:00-10:00  | Setup: Firebase project + Flutter config          |
| 🌅 10:00-12:00 | Firebase Messaging en Flutter (recepción)         |
| 🌞 12:00-13:00 | Backend: firebase-admin + API de envío            |
| 🌞 14:00-16:00 | Notificaciones por token + por topic              |
| 🌆 16:00-18:00 | Deep linking + datos en notificación              |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Centro de notificaciones en la app     |
| 🌅 10:30-12:00 | Notificaciones programadas             |
| 🌞 13:00-14:30 | Templates y segmentación por hotel     |
| 🌞 14:30-16:00 | Tests + preferencias de notificación   |
| 🌆 16:00-17:00 | README y documentación                 |

---

## ✅ Definición de "hecho"

- [ ] Push notifications funcionales (foreground/background)
- [ ] Envío desde backend a dispositivo y topic
- [ ] Centro de notificaciones en la app
- [ ] Deep linking funcional
- [ ] Docker Compose para backend
- [ ] README con documentación

---

## 💼 Lo que demuestra a Yuvod

| Habilidad       | Evidencia                                   |
| --------------- | ------------------------------------------- |
| Flutter         | Firebase integration, background handling    |
| Firebase        | Cloud Messaging, topics, data messages       |
| Node.js         | firebase-admin SDK en Express                |
| Engagement      | Notificaciones para mejorar experiencia      |
| Dominio hotel   | Alertas, promociones, recordatorios          |
