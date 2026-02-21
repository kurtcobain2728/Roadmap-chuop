# 🧪 Semana 08 — ReactTesting

> **Suite completa de tests unitarios y de integración en React con Jest, RTL y Cypress**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 25-26 de abril 2026 |
| 🏷️ Categoría       | Frontend Avanzado   |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

ReactTesting es un proyecto dedicado exclusivamente a dominar el testing en React. Toma los componentes de los proyectos anteriores (ChannelUI, DesignSystem) y construye una suite completa de tests: unitarios con Jest/Vitest + React Testing Library, e integración/E2E con Cypress.

Un Full Stack Developer profesional necesita _"Realizar tests unitarios y de integración continua"_ — este proyecto demuestra dominio total.

---

## ✨ Features

### Tests unitarios (Vitest + React Testing Library)

- [ ] Testing de componentes con render y queries
- [ ] Testing de hooks personalizados (renderHook)
- [ ] Testing de formularios con validación
- [ ] Testing de interacciones (click, type, select)
- [ ] Mocking de API calls (MSW - Mock Service Worker)
- [ ] Mocking de módulos y dependencias
- [ ] Snapshot testing

### Tests de integración (Cypress)

- [ ] Flujo completo de login/registro
- [ ] Navegación entre páginas
- [ ] CRUD desde la UI
- [ ] Interacciones con tablas (sort, filter, paginate)
- [ ] Tests de responsive (viewport resize)
- [ ] Tests de accesibilidad (a11y)

### CI/CD Integration

- [ ] GitHub Actions para correr tests en cada push
- [ ] Reporte de cobertura de código
- [ ] Visual regression con screenshots
- [ ] Tests como gate de calidad para PRs

---

## 🛠️ Stack técnico

| Tecnología                  | Propósito                   |
| --------------------------- | --------------------------- |
| **Vitest**                  | Test runner                 |
| **React Testing Library**   | Testing de componentes      |
| **MSW**                     | Mock de API calls           |
| **Cypress**                 | Tests E2E e integración     |
| **@testing-library/jest-dom**| Matchers DOM               |
| **@testing-library/user-event** | Simulación de eventos  |
| **istanbul/c8**             | Cobertura de código         |
| **GitHub Actions**          | CI/CD                       |

---

## 📁 Estructura del proyecto

```
react-testing/
├── src/
│   ├── components/          # Componentes a testear
│   │   ├── ChannelTable/
│   │   ├── LoginForm/
│   │   ├── ChannelForm/
│   │   └── Dashboard/
│   ├── hooks/
│   │   ├── useChannels.ts
│   │   └── useAuth.ts
│   ├── services/
│   │   └── api.ts
│   └── __tests__/
│       ├── components/
│       │   ├── ChannelTable.test.tsx
│       │   ├── LoginForm.test.tsx
│       │   ├── ChannelForm.test.tsx
│       │   └── Dashboard.test.tsx
│       ├── hooks/
│       │   ├── useChannels.test.ts
│       │   └── useAuth.test.ts
│       └── integration/
│           └── channelCRUD.test.tsx
├── cypress/
│   ├── e2e/
│   │   ├── login.cy.ts
│   │   ├── channels.cy.ts
│   │   └── navigation.cy.ts
│   ├── fixtures/
│   └── support/
├── mocks/
│   ├── handlers.ts          # MSW handlers
│   └── server.ts            # MSW server setup
├── .github/
│   └── workflows/
│       └── test.yml         # CI pipeline
├── package.json
├── vitest.config.ts
├── cypress.config.ts
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                          |
| -------------- | -------------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Vitest, RTL, MSW, Cypress                   |
| 🌅 10:00-12:00 | Tests unitarios de componentes (render, queries)    |
| 🌞 12:00-13:00 | Tests de hooks personalizados (renderHook)          |
| 🌞 14:00-16:00 | Mocking con MSW: API calls, error handling          |
| 🌆 16:00-18:00 | Tests de formularios e interacciones                |

### Domingo

| Hora           | Actividad                                    |
| -------------- | -------------------------------------------- |
| 🌅 9:00-10:30  | Cypress: setup + tests E2E de login          |
| 🌅 10:30-12:00 | Cypress: tests de CRUD y navegación          |
| 🌞 13:00-14:30 | Reporte de cobertura + GitHub Actions CI     |
| 🌞 14:30-16:00 | Tests de accesibilidad + visual regression   |
| 🌆 16:00-17:00 | README con reportes y badges de cobertura    |

---

## ✅ Definición de "hecho"

- [ ] Mínimo 30 tests unitarios pasando
- [ ] Cobertura ≥ 80%
- [ ] Mínimo 5 tests E2E con Cypress
- [ ] MSW configurado para mocking de API
- [ ] GitHub Actions corriendo tests en CI
- [ ] Reporte de cobertura generado
- [ ] README con guía de testing

---

## 💼 Valor para el portafolio

| Habilidad             | Evidencia                                 |
| --------------------- | ----------------------------------------- |
| Testing React         | RTL, hooks testing, snapshot testing       |
| Tests de integración  | Cypress E2E, MSW para mocking             |
| CI/CD                 | GitHub Actions con tests automáticos       |
| Clean code            | Código testeable = código bien diseñado    |
| Cobertura             | Métricas de calidad objetivas              |
| Mejores prácticas     | Testing como parte del flujo de desarrollo |
