# 📈 Semana 12 — AnalyticsDash

> **Dashboard de analíticas y métricas de uso del sistema con React + Express + MongoDB**

| Campo              | Detalle            |
| ------------------ | ------------------ |
| 📅 Fechas          | 23-24 de mayo 2026 |
| 🏷️ Categoría       | Full-Stack         |
| ⏱️ Tiempo estimado | 10-12 horas        |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio  |

---

## 🎯 Descripción

AnalyticsDash es un dashboard analítico full-stack que muestra métricas de uso: canales más vistos, horarios pico, contenido VOD popular, engagement por hotel, y tendencias. Usa **MongoDB Aggregation Pipelines** para procesar datos y **Chart.js** para visualizarlos.

---

## ✨ Features

### Frontend
- [ ] Dashboard con KPIs principales (tarjetas de métricas)
- [ ] Gráfico de líneas: tendencias de viewership en el tiempo
- [ ] Gráfico de barras: canales más populares
- [ ] Gráfico de dona: distribución por categoría de contenido
- [ ] Tabla de ranking: hoteles con más engagement
- [ ] Filtros por rango de fechas, hotel, tipo de contenido
- [ ] Exportar reportes a PDF/CSV

### Backend
- [ ] API de analíticas con MongoDB Aggregation Pipelines
- [ ] Endpoints con filtros de fechas y agrupaciones
- [ ] Caching de resultados con Redis (o caché en memoria)
- [ ] Seed de datos de ejemplo para demostración
- [ ] PostgreSQL como alternativa para queries analíticas complejas

---

## 🛠️ Stack técnico

| Tecnología          | Propósito            |
| ------------------- | -------------------- |
| **React 18+**       | Frontend             |
| **Chart.js**        | Gráficos             |
| **Material UI**     | UI                   |
| **Express.js**      | Backend              |
| **MongoDB**         | Datos + Aggregation  |
| **PostgreSQL**      | Queries analíticas   |
| **Docker Compose**  | Infraestructura      |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                         |
| -------------- | ------------------------------------------------- |
| 🌅 9:00-10:00  | Setup + seed de datos de ejemplo                   |
| 🌅 10:00-12:00 | Backend: Aggregation Pipelines para métricas       |
| 🌞 12:00-13:00 | Endpoints de analíticas con filtros                |
| 🌞 14:00-16:00 | Frontend: layout del dashboard con gráficos        |
| 🌆 16:00-18:00 | Gráficos: líneas, barras, dona con Chart.js        |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Tabla de ranking + filtros             |
| 🌅 10:30-12:00 | Exportar a PDF/CSV                     |
| 🌞 13:00-14:30 | PostgreSQL: queries analíticas         |
| 🌞 14:30-16:00 | Tests + caching                        |
| 🌆 16:00-17:00 | README con screenshots                 |

---

## ✅ Definición de "hecho"

- [ ] Dashboard con al menos 4 tipos de visualización
- [ ] Filtros por fechas y categorías
- [ ] MongoDB Aggregation Pipelines funcionales
- [ ] Exportación a CSV/PDF
- [ ] Docker Compose funcional
- [ ] README con screenshots

---

## 💼 Valor para el portafolio

| Habilidad       | Evidencia                                   |
| --------------- | ------------------------------------------- |
| MongoDB avanzado| Aggregation Pipelines para analíticas       |
| PostgreSQL      | Queries analíticas como tecnología valorable|
| React + Charts  | Visualizaciones interactivas                |
| Full-stack      | Frontend + Backend integrados               |
| Datos           | Transformación de datos en insights         |
