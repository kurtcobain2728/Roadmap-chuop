# 🔌 Semana 20 — DartAPI

> **Cliente API en Dart con integración completa al backend Node.js/Express**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 18-19 de julio 2026 |
| 🏷️ Categoría       | Flutter & Mobile    |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

DartAPI es un proyecto que demuestra la integración completa entre una app Flutter y el backend Node.js/Express/MongoDB. Implementa un cliente API robusto en Dart con: autenticación JWT, interceptors, caching, error handling, y modelos tipados con serialización automática.

---

## ✨ Features

### Cliente API
- [ ] Clase ApiClient centralizada con Dio
- [ ] Interceptors para: auth token, logging, retry, error handling
- [ ] Refresh token automático cuando el access token expira
- [ ] Serialización/deserialización automática con json_serializable
- [ ] Modelos tipados para todas las respuestas de API
- [ ] Manejo de errores centralizado (ApiException)

### Autenticación
- [ ] Login con email/password
- [ ] Registro de usuario
- [ ] Token storage seguro (flutter_secure_storage)
- [ ] Auto-login con refresh token
- [ ] Logout con limpieza de tokens

### Funcionalidades
- [ ] CRUD completo de canales desde la app
- [ ] Listado de contenido VOD con paginación
- [ ] Perfil de usuario (ver/editar)
- [ ] Búsqueda con debounce

### Offline Support
- [ ] Caché de respuestas con Hive
- [ ] Indicador de conexión
- [ ] Retry automático cuando vuelve la conexión

---

## 🛠️ Stack técnico

| Tecnología                | Propósito                  |
| ------------------------- | -------------------------- |
| **Flutter 3+**            | Framework UI               |
| **Dart**                  | Lenguaje                   |
| **Dio**                   | HTTP client                |
| **json_serializable**     | Serialización              |
| **flutter_secure_storage**| Token storage              |
| **Hive**                  | Caché local                |
| **Riverpod**              | State management           |
| **Express.js (backend)**  | API a consumir             |
| **MongoDB (backend)**     | Base de datos              |

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                        |
| -------------- | ------------------------------------------------ |
| 🌅 9:00-10:00  | Setup: Dio, modelos, json_serializable            |
| 🌅 10:00-12:00 | ApiClient + interceptors (auth, log, retry)       |
| 🌞 12:00-13:00 | Auth flow: login, registro, token management      |
| 🌞 14:00-16:00 | CRUD de canales + listado VOD con paginación      |
| 🌆 16:00-18:00 | Error handling centralizado + UI de errores       |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Caché offline con Hive                 |
| 🌅 10:30-12:00 | Búsqueda con debounce                  |
| 🌞 13:00-14:30 | Perfil de usuario + edición            |
| 🌞 14:30-16:00 | Tests unitarios del API client         |
| 🌆 16:00-17:00 | README y documentación                 |

---

## ✅ Definición de "hecho"

- [ ] ApiClient con interceptors funcional
- [ ] Auth flow completo (login/registro/refresh)
- [ ] CRUD consumiendo API real
- [ ] Caché offline funcional
- [ ] Error handling robusto
- [ ] Tests del API client
- [ ] README con documentación

---

## 💼 Valor para el portafolio

| Habilidad       | Evidencia                                   |
| --------------- | ------------------------------------------- |
| Dart            | Package de API client profesional           |
| Flutter         | Integración UI + API robusta                |
| Integración API | Consumo de Express API desde Flutter        |
| Auth            | JWT flow completo en mobile                 |
| Offline         | Caché y manejo de conectividad              |
