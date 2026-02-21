# 📊 Semana 07 — LivePanel

> **Panel de monitoreo en tiempo real con React, WebSockets y Chart.js**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 18-19 de abril 2026 |
| 🏷️ Categoría       | Frontend Avanzado   |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

LivePanel es un panel de monitoreo en tiempo real que muestra métricas live de un sistema de TV en la nube: señales activas, viewers por canal, calidad de stream, alertas y logs de eventos. Usa **WebSockets** para recibir datos en tiempo real y **Chart.js** para visualizaciones interactivas.

Simula el tipo de herramientas de monitoreo que un equipo como Yuvod necesitaría para supervisar su plataforma.

---

## ✨ Features

### Dashboard en tiempo real

- [ ] Métricas live actualizándose cada segundo
- [ ] Gráfico de líneas: viewers por canal en el tiempo
- [ ] Gráfico de barras: distribución de viewers por canal
- [ ] Gráfico de dona: estado de señales (activas/inactivas/error)
- [ ] Mapa de calor: actividad por hora del día
- [ ] Indicadores de salud del sistema

### WebSockets

- [ ] Conexión WebSocket persistente con reconnect
- [ ] Suscripción a diferentes canales de eventos
- [ ] Manejo de estados de conexión (connected, reconnecting, error)
- [ ] Buffer de mensajes durante desconexión

### Alertas y notificaciones

- [ ] Alertas en tiempo real (señal caída, error de stream)
- [ ] Historial de alertas con filtros
- [ ] Notificaciones sonoras opcionales
- [ ] Badge de alertas no leídas

### Experiencia

- [ ] Auto-refresh configurable
- [ ] Rango de tiempo seleccionable (últimos 5min, 1h, 24h)
- [ ] Exportar datos a CSV
- [ ] Responsive y dark mode

---

## 🛠️ Stack técnico

| Tecnología              | Propósito                    |
| ----------------------- | ---------------------------- |
| **React 18+**           | UI                           |
| **TypeScript**          | Tipado estricto              |
| **Socket.io Client**    | WebSockets                   |
| **Chart.js + react-chartjs-2** | Gráficos             |
| **Material UI (MUI)**   | Componentes UI               |
| **Zustand**             | Estado global (métricas)     |
| **date-fns**            | Manejo de timestamps         |
| **Vite**                | Build tool                   |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                     |
| -------------- | --------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Vite + React + TS + Socket.io + Chart.js|
| 🌅 10:00-12:00 | Backend mock con WebSocket server (Express)    |
| 🌞 12:00-13:00 | Layout del dashboard con MUI Grid              |
| 🌞 14:00-16:00 | Gráficos: líneas, barras, dona con Chart.js    |
| 🌆 16:00-18:00 | Conexión WebSocket + actualización en tiempo real|

### Domingo

| Hora           | Actividad                                |
| -------------- | ---------------------------------------- |
| 🌅 9:00-10:30  | Indicadores de salud + métricas live     |
| 🌅 10:30-12:00 | Sistema de alertas en tiempo real        |
| 🌞 13:00-14:30 | Dark mode, responsive, exportar CSV      |
| 🌞 14:30-16:00 | Tests de componentes                     |
| 🌆 16:00-17:00 | README con screenshots/GIFs             |

---

## ✅ Definición de "hecho"

- [ ] Dashboard con al menos 4 tipos de gráficos
- [ ] Datos actualizándose en tiempo real via WebSocket
- [ ] Sistema de alertas funcional
- [ ] Responsive y dark mode
- [ ] Manejo de reconexión WebSocket
- [ ] Tests de componentes
- [ ] README con screenshots

---

## 💼 Lo que demuestra a Yuvod

| Habilidad         | Evidencia                                    |
| ----------------- | -------------------------------------------- |
| React avanzado    | WebSockets, Chart.js, estado reactivo        |
| Tiempo real       | Datos live actualizándose cada segundo       |
| Monitoreo         | Dashboard de métricas del sistema TV         |
| Material UI       | Componentes MUI con personalización          |
| Dominio Yuvod     | Monitoreo de señales, viewers, calidad       |
| UX                | Alertas, dark mode, exportación de datos     |
