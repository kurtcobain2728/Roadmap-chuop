# 📺 Semana 03 — ContentDB

> **Servicio de gestión de contenido multimedia (catálogo TV/VOD) con MongoDB avanzado**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 21-22 de marzo 2026 |
| 🏷️ Categoría       | Backend Foundations |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

ContentDB es un servicio de gestión de contenido multimedia diseñado para un sistema de TV en la nube — un dominio real y demandado. Gestiona canales de TV, programación, contenido VOD (video bajo demanda), y categorías. Usa **MongoDB avanzado** con aggregation pipelines, índices compuestos, y population de documentos relacionados.

---

## 🏗️ Arquitectura

```
┌─────────────────────────────┐
│        Express API          │
│   (Content Management)      │
└──────────┬──────────────────┘
           │
    ┌──────┼──────┐
    │      │      │
┌───▼──┐┌──▼──┐┌──▼────┐
│Channe││ VOD ││Program│
│  ls  ││     ││ ming  │
└───┬──┘└──┬──┘└──┬────┘
    │      │      │
    └──────┼──────┘
           │
    ┌──────▼──────┐
    │  MongoDB     │
    │ (GridFS para │
    │  assets)     │
    └─────────────┘
```

---

## ✨ Features

### Gestión de canales de TV

- [ ] CRUD de canales (nombre, número, logo, género, idioma)
- [ ] Categorías de canales (deportes, noticias, entretenimiento, etc.)
- [ ] Estado del canal (activo, inactivo, mantenimiento)
- [ ] Ordenamiento y priorización de canales por hotel
- [ ] Paquetes de canales configurables

### Contenido VOD

- [ ] CRUD de contenido VOD (películas, series, documentales)
- [ ] Metadatos ricos: título, sinopsis, duración, género, clasificación
- [ ] Categorización y etiquetado
- [ ] Contenido destacado y recomendaciones
- [ ] Disponibilidad por período de tiempo

### Programación (EPG)

- [ ] Guía de programación electrónica (EPG)
- [ ] Programación por horario y canal
- [ ] Importación de datos de programación (XML/JSON)
- [ ] Consulta de "qué hay ahora" y "próximamente"

### MongoDB Avanzado

- [ ] Aggregation pipelines para reportes y estadísticas
- [ ] Índices compuestos para búsquedas eficientes
- [ ] Population de documentos relacionados
- [ ] Text indexes para búsqueda full-text
- [ ] Validación a nivel de schema de MongoDB

---

## 🛠️ Stack técnico

| Tecnología          | Propósito                          |
| ------------------- | ---------------------------------- |
| **Express.js**      | Framework web                      |
| **TypeScript**      | Tipado estricto                    |
| **MongoDB**         | Base de datos documento            |
| **Mongoose**        | ODM con schemas avanzados          |
| **Zod**             | Validación de inputs               |
| **Docker Compose**  | Infraestructura local              |
| **Vitest**          | Testing                            |
| **Supertest**       | Testing HTTP                       |
| **multer**          | Upload de archivos (logos, posters)|

---

## 📡 Endpoints de la API

```
# Canales
GET    /api/v1/channels              # Listar canales (filtros, paginación)
POST   /api/v1/channels              # Crear canal
GET    /api/v1/channels/:id          # Obtener canal con programación
PUT    /api/v1/channels/:id          # Actualizar canal
DELETE /api/v1/channels/:id          # Eliminar canal
GET    /api/v1/channels/categories   # Listar categorías

# VOD
GET    /api/v1/vod                   # Listar contenido VOD
POST   /api/v1/vod                   # Crear contenido VOD
GET    /api/v1/vod/:id               # Obtener detalle de contenido
PUT    /api/v1/vod/:id               # Actualizar contenido
DELETE /api/v1/vod/:id               # Eliminar contenido
GET    /api/v1/vod/featured          # Contenido destacado

# EPG
GET    /api/v1/epg/:channelId        # Programación de un canal
POST   /api/v1/epg                   # Crear entrada de programación
GET    /api/v1/epg/now               # Qué hay ahora en todos los canales
GET    /api/v1/epg/next/:channelId   # Próximo programa
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                            |
| -------------- | ---------------------------------------------------- |
| 🌅 9:00-10:00  | Setup del proyecto, Docker Compose, dependencias     |
| 🌅 10:00-12:00 | Modelos Mongoose: Channel, VODContent, EPGEntry      |
| 🌞 12:00-13:00 | Schemas Zod + Service layer de canales               |
| 🌞 14:00-16:00 | CRUD completo de canales + categorías                |
| 🌆 16:00-18:00 | CRUD de contenido VOD + metadatos                    |

### Domingo

| Hora           | Actividad                                    |
| -------------- | -------------------------------------------- |
| 🌅 9:00-10:30  | EPG: programación por canal y horario        |
| 🌅 10:30-12:00 | Aggregation pipelines + índices compuestos   |
| 🌞 13:00-14:30 | Tests con Vitest + fixtures de datos         |
| 🌞 14:30-16:00 | Búsqueda full-text + filtros avanzados       |
| 🌆 16:00-17:00 | README y documentación Swagger               |

---

## ✅ Definición de "hecho"

- [ ] CRUD completo de canales, VOD y EPG
- [ ] Aggregation pipelines para estadísticas
- [ ] Índices optimizados para búsquedas frecuentes
- [ ] Búsqueda full-text funcional
- [ ] Tests con buena cobertura
- [ ] Docker Compose funcional
- [ ] README con instrucciones y ejemplos

---

## 💼 Valor para el portafolio

| Habilidad        | Evidencia                                       |
| ---------------- | ----------------------------------------------- |
| MongoDB avanzado | Aggregations, indices, populate, text search    |
| Dominio del negocio    | Canales TV, VOD, EPG — el core del negocio      |
| Node.js/Express  | API REST bien estructurada y documentada        |
| TypeScript       | Tipos estrictos para todo el contenido          |
| Modelado datos   | Relaciones entre canales, contenido y programas |
| Escalabilidad    | Queries optimizadas con índices compuestos      |
