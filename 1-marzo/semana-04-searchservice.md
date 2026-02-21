# 🔍 Semana 04 — SearchService

> **Motor de búsqueda avanzada con Elasticsearch, Express y MongoDB**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 28-29 de marzo 2026 |
| 🏷️ Categoría       | Backend Foundations |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

SearchService es un microservicio de búsqueda avanzada que utiliza **Elasticsearch** para indexar contenido de canales TV, VOD y hoteles, permitiendo búsquedas rápidas, autocompletado, filtros facetados y resultados relevantes. Se sincroniza con MongoDB como fuente de verdad.

Elasticsearch es una tecnología muy valorada en la industria — este proyecto demuestra dominio práctico.

---

## 🏗️ Arquitectura

```
┌──────────────────────┐
│    Express API       │
│  (Search Endpoints)  │
└──────────┬───────────┘
           │
    ┌──────┴──────┐
    │             │
┌───▼────┐  ┌────▼──────┐
│Elastic │  │  MongoDB   │
│Search  │  │ (Source of │
│(Index) │  │  Truth)    │
└───┬────┘  └────┬──────┘
    │             │
    └──────┬──────┘
           │
    ┌──────▼──────┐
    │  Sync Job   │
    │ (Indexer)   │
    └─────────────┘
```

---

## ✨ Features

### Búsqueda

- [ ] Búsqueda full-text con relevancia
- [ ] Autocompletado (suggest API)
- [ ] Búsqueda fuzzy (tolerante a errores)
- [ ] Filtros facetados (género, tipo, idioma, rating)
- [ ] Highlighting de términos buscados
- [ ] Ordenamiento por relevancia, fecha, popularidad

### Indexación

- [ ] Sincronización MongoDB → Elasticsearch
- [ ] Indexación en tiempo real (Change Streams)
- [ ] Re-indexación completa bajo demanda
- [ ] Mappings tipados para cada tipo de contenido
- [ ] Analyzers personalizados (español + inglés)

### API

- [ ] Endpoint de búsqueda unificada (canales + VOD + hoteles)
- [ ] Endpoint de sugerencias/autocompletado
- [ ] Endpoint de búsquedas populares
- [ ] Health check y estadísticas del índice

---

## 🛠️ Stack técnico

| Tecnología             | Propósito                          |
| ---------------------- | ---------------------------------- |
| **Express.js**         | Framework web                      |
| **TypeScript**         | Tipado estricto                    |
| **Elasticsearch 8.x**  | Motor de búsqueda                  |
| **@elastic/elasticsearch** | Cliente oficial ES para Node.js |
| **MongoDB**            | Fuente de verdad de datos          |
| **Mongoose**           | ODM                                |
| **Docker Compose**     | Infraestructura (ES + MongoDB)     |
| **Vitest**             | Testing                            |

---

## 📡 Endpoints de la API

```
GET  /api/v1/search?q=...&type=...&genre=...    # Búsqueda unificada
GET  /api/v1/search/suggest?q=...                # Autocompletado
GET  /api/v1/search/popular                      # Búsquedas populares

POST /api/v1/index/sync                          # Sincronizar MongoDB → ES
POST /api/v1/index/reindex                       # Re-indexación completa
GET  /api/v1/index/stats                         # Estadísticas del índice

GET  /api/v1/health                              # Health check
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                             |
| -------------- | ----------------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Express, Elasticsearch, Docker Compose          |
| 🌅 10:00-12:00 | Mappings de ES + analyzers personalizados              |
| 🌞 12:00-13:00 | Job de sincronización MongoDB → Elasticsearch          |
| 🌞 14:00-16:00 | Endpoint de búsqueda con filtros facetados             |
| 🌆 16:00-18:00 | Autocompletado + búsqueda fuzzy + highlighting         |

### Domingo

| Hora           | Actividad                                    |
| -------------- | -------------------------------------------- |
| 🌅 9:00-10:30  | Change Streams para indexación en tiempo real|
| 🌅 10:30-12:00 | Re-indexación completa + estadísticas        |
| 🌞 13:00-14:30 | Tests con contenedores de test (testcontainers)|
| 🌞 14:30-16:00 | Optimización de queries y relevancia         |
| 🌆 16:00-17:00 | README y documentación                       |

---

## ✅ Definición de "hecho"

- [ ] Búsqueda full-text funcional con resultados relevantes
- [ ] Autocompletado con sugerencias
- [ ] Filtros facetados (mínimo 3 facetas)
- [ ] Sincronización MongoDB → Elasticsearch
- [ ] Docker Compose con ES + MongoDB + App
- [ ] Tests con buena cobertura
- [ ] README con instrucciones y ejemplos

---

## 💼 Valor para el portafolio

| Habilidad       | Evidencia                                  |
| --------------- | ------------------------------------------ |
| Elasticsearch   | Mappings, analyzers, búsqueda avanzada     |
| Node.js/Express | Microservicio de búsqueda profesional      |
| MongoDB         | Change Streams, sincronización             |
| Dominio del negocio   | Búsqueda de canales, VOD, hoteles          |
| Escalabilidad   | Arquitectura preparada para alto volumen   |
| DevOps          | Docker Compose multi-servicio              |
