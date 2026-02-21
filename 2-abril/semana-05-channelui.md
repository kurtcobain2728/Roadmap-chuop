# 📺 Semana 05 — ChannelUI

> **Dashboard de gestión de canales de TV con React, TypeScript y Material UI**

| Campo              | Detalle           |
| ------------------ | ----------------- |
| 📅 Fechas          | 4-5 de abril 2026 |
| 🏷️ Categoría       | Frontend Avanzado |
| ⏱️ Tiempo estimado | 10-12 horas       |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio |

---

## 🎯 Descripción

ChannelUI es un dashboard de gestión de canales de televisión construido con **React, TypeScript y Material UI**. Permite administrar canales, ver programación, gestionar paquetes y monitorear el estado de las señales. Consume la API de ContentDB (Semana 03) como backend.

Replica directamente una interfaz que un equipo del sector necesitaría para gestionar su plataforma de TV en la nube.

---

## ✨ Features

### Dashboard principal

- [ ] Vista general con estadísticas (canales activos, usuarios, señales)
- [ ] Cards con métricas clave usando gráficos
- [ ] Barra de navegación lateral con Material UI
- [ ] Breadcrumbs y navegación intuitiva
- [ ] Theme switching (dark/light mode)

### Gestión de canales

- [ ] Tabla de canales con sorting y filtros
- [ ] Formulario de crear/editar canal con validación
- [ ] Vista de detalle de canal con programación
- [ ] Drag & drop para reordenar canales
- [ ] Upload de logos con preview

### Programación (EPG)

- [ ] Vista de grilla de programación por horario
- [ ] Timeline interactivo
- [ ] Detalle de programa al hacer click

### Experiencia de usuario

- [ ] Responsive design (desktop + tablet)
- [ ] Skeleton loaders durante carga
- [ ] Toasts para notificaciones
- [ ] Confirmaciones de acciones destructivas
- [ ] Atajos de teclado

---

## 🛠️ Stack técnico

| Tecnología            | Propósito                       |
| --------------------- | ------------------------------- |
| **React 18+**         | Librería UI                     |
| **TypeScript**        | Tipado estricto                 |
| **Material UI (MUI)** | Design system / componentes     |
| **React Router**      | Navegación                      |
| **React Query**       | Data fetching y cache           |
| **Zustand**           | Estado global                   |
| **Vite**              | Build tool                      |
| **Axios**             | HTTP client                     |
| **date-fns**          | Manejo de fechas                |

---

## 📁 Estructura del proyecto

```
channelui/
├── src/
│   ├── main.tsx                 # Entry point
│   ├── App.tsx                  # App con router y providers
│   ├── components/
│   │   ├── layout/
│   │   │   ├── Sidebar.tsx      # Navegación lateral
│   │   │   ├── Header.tsx       # Barra superior
│   │   │   └── MainLayout.tsx   # Layout principal
│   │   ├── channels/
│   │   │   ├── ChannelTable.tsx  # Tabla de canales
│   │   │   ├── ChannelForm.tsx   # Formulario crear/editar
│   │   │   ├── ChannelCard.tsx   # Card de canal
│   │   │   └── ChannelDetail.tsx # Vista de detalle
│   │   ├── epg/
│   │   │   ├── EPGGrid.tsx      # Grilla de programación
│   │   │   └── ProgramCard.tsx  # Card de programa
│   │   └── common/
│   │       ├── StatsCard.tsx    # Card de estadísticas
│   │       ├── SearchBar.tsx    # Barra de búsqueda
│   │       └── ConfirmDialog.tsx # Dialog de confirmación
│   ├── hooks/
│   │   ├── useChannels.ts       # Custom hook para canales
│   │   ├── useEPG.ts            # Custom hook para programación
│   │   └── useTheme.ts          # Custom hook para tema
│   ├── services/
│   │   ├── api.ts               # Configuración Axios
│   │   ├── channelService.ts    # API de canales
│   │   └── epgService.ts        # API de EPG
│   ├── stores/
│   │   └── uiStore.ts           # Estado global UI (Zustand)
│   ├── types/
│   │   ├── channel.ts           # Tipos de canal
│   │   └── epg.ts               # Tipos de EPG
│   ├── pages/
│   │   ├── Dashboard.tsx        # Página principal
│   │   ├── ChannelList.tsx      # Lista de canales
│   │   ├── ChannelDetailPage.tsx # Detalle de canal
│   │   └── EPGPage.tsx          # Página de programación
│   └── theme/
│       └── muiTheme.ts          # Personalización MUI theme
├── package.json
├── tsconfig.json
├── vite.config.ts
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                             |
| -------------- | ----------------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Vite + React + TypeScript + MUI                |
| 🌅 10:00-12:00 | Layout principal: Sidebar, Header, routing            |
| 🌞 12:00-13:00 | Dashboard con StatsCards y gráficos                   |
| 🌞 14:00-16:00 | Tabla de canales con sorting, filtros, paginación     |
| 🌆 16:00-18:00 | Formulario de canales + validación                    |

### Domingo

| Hora           | Actividad                                |
| -------------- | ---------------------------------------- |
| 🌅 9:00-10:30  | Vista de detalle de canal                |
| 🌅 10:30-12:00 | Grilla EPG interactiva                   |
| 🌞 13:00-14:30 | Dark mode, responsive, polish            |
| 🌞 14:30-16:00 | Integración con API backend              |
| 🌆 16:00-17:00 | README con screenshots                   |

---

## ✅ Definición de "hecho"

- [ ] Dashboard funcional con métricas
- [ ] CRUD de canales desde la UI
- [ ] Vista EPG interactiva
- [ ] Dark/Light mode
- [ ] Responsive (desktop + tablet)
- [ ] TypeScript estricto
- [ ] README con screenshots

---

## 💼 Valor para el portafolio

| Habilidad             | Evidencia                                  |
| --------------------- | ------------------------------------------ |
| ReactJS avanzado      | Hooks, lazy loading, React Query           |
| Material UI           | Componentes MUI personalizados             |
| TypeScript            | Tipado estricto en componentes y hooks      |
| UX/UI                 | Dashboard intuitivo, responsive, dark mode |
| Dominio del negocio         | Gestión de canales TV — core del negocio   |
| Integración frontend  | Consumo de API REST con React Query        |
