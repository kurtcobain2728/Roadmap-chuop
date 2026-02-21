# 🧩 Semana 06 — DesignSystem

> **Librería de componentes reutilizables profesional con React, Storybook y Material Design**

| Campo              | Detalle            |
| ------------------ | ------------------ |
| 📅 Fechas          | 11-12 de abril 2026|
| 🏷️ Categoría       | Frontend Avanzado  |
| ⏱️ Tiempo estimado | 10-12 horas        |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio  |

---

## 🎯 Descripción

DesignSystem es una librería de componentes React reutilizables documentada con **Storybook**, siguiendo principios de **Material Design**. Incluye botones, inputs, cards, tablas, modals, toast notifications, y más — todos tipados con TypeScript, testeados y con variantes configurables.

La industria valora _"construir y mantener componentes reutilizables y arquitectura frontend"_.

---

## ✨ Features

### Componentes

- [ ] **Button**: variantes (primary, secondary, outlined, text), tamaños, loading state
- [ ] **Input**: text, password, email, number, textarea, con validación visual
- [ ] **Select**: dropdown con búsqueda, multi-select, chips
- [ ] **Card**: variantes (estadísticas, contenido, media)
- [ ] **DataTable**: sorting, filtros, paginación, selección, row actions
- [ ] **Modal/Dialog**: confirmación, formularios, información
- [ ] **Toast/Snackbar**: success, error, warning, info, con auto-dismiss
- [ ] **Badge/Chip**: estados, categorías, etiquetas
- [ ] **Avatar**: imágenes, iniciales, estados online/offline
- [ ] **Skeleton**: placeholders para loading states

### Design Tokens

- [ ] Paleta de colores (primary, secondary, neutral, semantic)
- [ ] Tipografía (font family, sizes, weights, line heights)
- [ ] Spacing scale (4px base)
- [ ] Border radius, shadows, transitions
- [ ] Breakpoints responsive

### Documentación

- [ ] Storybook con todas las variantes de cada componente
- [ ] Controles interactivos (knobs/controls)
- [ ] Documentación de uso y props
- [ ] Ejemplos de composición de componentes
- [ ] Guía de contribución

---

## 🛠️ Stack técnico

| Tecnología            | Propósito                   |
| --------------------- | --------------------------- |
| **React 18+**         | Librería UI                 |
| **TypeScript**        | Tipado de componentes       |
| **Material UI (MUI)** | Base de componentes         |
| **Storybook 7+**      | Documentación visual        |
| **Emotion/styled**    | CSS-in-JS                   |
| **Vite**              | Build tool                  |
| **Vitest**            | Tests unitarios             |
| **Chromatic**         | Visual regression testing   |

---

## 📁 Estructura del proyecto

```
designsystem/
├── src/
│   ├── components/
│   │   ├── Button/
│   │   │   ├── Button.tsx
│   │   │   ├── Button.test.tsx
│   │   │   ├── Button.stories.tsx
│   │   │   └── index.ts
│   │   ├── Input/
│   │   ├── Select/
│   │   ├── Card/
│   │   ├── DataTable/
│   │   ├── Modal/
│   │   ├── Toast/
│   │   ├── Badge/
│   │   ├── Avatar/
│   │   └── Skeleton/
│   ├── theme/
│   │   ├── tokens.ts          # Design tokens
│   │   ├── palette.ts         # Colores
│   │   ├── typography.ts      # Tipografía
│   │   └── theme.ts           # MUI theme completo
│   ├── hooks/
│   │   └── useThemeMode.ts    # Hook dark/light
│   └── index.ts               # Barrel exports
├── .storybook/
│   ├── main.ts
│   └── preview.ts
├── package.json
├── tsconfig.json
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Vite + React + TS + Storybook + MUI      |
| 🌅 10:00-11:00 | Design tokens: colores, tipografía, spacing      |
| 🌞 11:00-13:00 | Componentes: Button, Input, Select               |
| 🌞 14:00-16:00 | Componentes: Card, Badge, Avatar, Skeleton       |
| 🌆 16:00-18:00 | Componentes: DataTable + Modal                   |

### Domingo

| Hora           | Actividad                              |
| -------------- | -------------------------------------- |
| 🌅 9:00-10:30  | Componente: Toast/Snackbar             |
| 🌅 10:30-12:00 | Stories de Storybook para todo         |
| 🌞 13:00-14:30 | Tests unitarios de componentes         |
| 🌞 14:30-16:00 | Documentación y guía de uso            |
| 🌆 16:00-17:00 | README y publicación                   |

---

## ✅ Definición de "hecho"

- [ ] Mínimo 10 componentes funcionales
- [ ] Storybook con todas las variantes documentadas
- [ ] Design tokens configurados
- [ ] Dark/Light mode funcionando
- [ ] Tests unitarios para cada componente
- [ ] TypeScript estricto en todos los componentes
- [ ] README con instrucciones de uso

---

## 💼 Valor para el portafolio

| Habilidad                     | Evidencia                               |
| ----------------------------- | --------------------------------------- |
| Componentes reutilizables     | Librería completa con Storybook         |
| Material Design               | MUI personalizado con design tokens     |
| TypeScript                    | Props tipadas, generics en componentes  |
| Testing frontend              | Tests de render, interacción, props     |
| Arquitectura frontend         | Organización modular, barrel exports    |
| Colaboración UX/UI            | Storybook como puente con diseñadores   |
