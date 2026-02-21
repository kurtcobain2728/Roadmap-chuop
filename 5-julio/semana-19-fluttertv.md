# 📺 Semana 19 — FlutterTV

> **App móvil de control de TV para huéspedes de hotel con Flutter, Dart y Material Design**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 11-12 de julio 2026 |
| 🏷️ Categoría       | Flutter & Mobile    |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

FlutterTV es una app móvil que permite a los huéspedes de un hotel controlar la TV de su habitación desde su teléfono: cambiar de canal, ver la guía de programación, acceder a contenido VOD, y controlar el volumen. Todo construido con **Flutter y Dart** usando **Material Design 3**.

Un control remoto móvil para un sistema de TV en la nube — proyecto ideal para demostrar dominio de Flutter.

---

## ✨ Features

### Control de TV
- [ ] Lista de canales disponibles con logo y nombre
- [ ] Cambiar de canal con un toque
- [ ] Control de volumen (slider)
- [ ] Botones de navegación (arriba, abajo, OK, atrás)
- [ ] Apagar/encender TV

### Guía de programación
- [ ] EPG (Electronic Program Guide) por canal
- [ ] Vista de "ahora en TV" con progreso
- [ ] Vista de próximos programas
- [ ] Búsqueda de programas

### Contenido VOD
- [ ] Catálogo de películas y series
- [ ] Carruseles por categoría
- [ ] Detalle de contenido con sinopsis
- [ ] Botón de reproducir en TV

### UX Móvil
- [ ] Material Design 3 (Material You)
- [ ] Dark/Light mode automático
- [ ] Animaciones y transiciones fluidas
- [ ] Splash screen y onboarding
- [ ] Bottom navigation

---

## 🛠️ Stack técnico

| Tecnología           | Propósito                    |
| -------------------- | ---------------------------- |
| **Flutter 3+**       | Framework UI                 |
| **Dart**             | Lenguaje de programación     |
| **Material Design 3**| Sistema de diseño            |
| **go_router**        | Navegación                   |
| **Riverpod**         | State management             |
| **http/dio**         | HTTP client                  |
| **flutter_test**     | Testing                      |

---

## 📁 Estructura del proyecto

```
flutter_tv/
├── lib/
│   ├── main.dart                  # Entry point
│   ├── app.dart                   # MaterialApp config
│   ├── router/
│   │   └── app_router.dart        # go_router setup
│   ├── features/
│   │   ├── remote/
│   │   │   ├── screens/
│   │   │   │   └── remote_screen.dart
│   │   │   └── widgets/
│   │   │       ├── channel_grid.dart
│   │   │       ├── volume_slider.dart
│   │   │       └── nav_pad.dart
│   │   ├── epg/
│   │   │   ├── screens/
│   │   │   │   └── epg_screen.dart
│   │   │   └── widgets/
│   │   │       └── program_card.dart
│   │   ├── vod/
│   │   │   ├── screens/
│   │   │   │   ├── vod_catalog.dart
│   │   │   │   └── vod_detail.dart
│   │   │   └── widgets/
│   │   │       └── content_carousel.dart
│   │   └── auth/
│   │       └── screens/
│   │           └── login_screen.dart
│   ├── models/
│   │   ├── channel.dart
│   │   ├── program.dart
│   │   └── vod_content.dart
│   ├── providers/
│   │   ├── channel_provider.dart
│   │   ├── epg_provider.dart
│   │   └── vod_provider.dart
│   ├── services/
│   │   └── api_service.dart
│   └── theme/
│       └── app_theme.dart         # Material 3 theme
├── test/
│   ├── widget_test.dart
│   └── unit_test.dart
├── pubspec.yaml
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado
| Hora           | Actividad                                        |
| -------------- | ------------------------------------------------ |
| 🌅 9:00-10:00  | Setup: Flutter project, Material 3 theme          |
| 🌅 10:00-12:00 | Pantalla de control remoto: canales + volumen     |
| 🌞 12:00-13:00 | Navegación con go_router + bottom nav             |
| 🌞 14:00-16:00 | Guía de programación (EPG)                        |
| 🌆 16:00-18:00 | Catálogo VOD: carruseles + detalle                |

### Domingo
| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | State management con Riverpod          |
| 🌅 10:30-12:00 | Integración con API mock               |
| 🌞 13:00-14:30 | Dark mode + animaciones                |
| 🌞 14:30-16:00 | Tests de widgets                       |
| 🌆 16:00-17:00 | README con screenshots                 |

---

## ✅ Definición de "hecho"

- [ ] App funcional con control de TV
- [ ] Lista de canales y EPG
- [ ] Catálogo VOD con categorías
- [ ] Material Design 3 implementado
- [ ] Dark/Light mode
- [ ] State management con Riverpod
- [ ] Tests de widgets básicos
- [ ] README con screenshots

---

## 💼 Valor para el portafolio

| Habilidad         | Evidencia                                   |
| ----------------- | ------------------------------------------- |
| Flutter/Dart      | App completa con Material Design 3          |
| Dominio del negocio     | Control remoto de TV — producto real         |
| Material Design   | Material You en Flutter                     |
| State management  | Riverpod patterns                           |
| UX móvil          | Navegación, animaciones, dark mode          |
| Multiplataforma   | iOS + Android desde una base de código      |
