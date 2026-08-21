# Estructura Estándar de Proyecto Web

Especifica las carpetas y archivos estándar reconocidos en proyectos Web modernos (Svelte/SvelteKit, React/Next.js, Vue/Nuxt, Astro). Durante el protocolo de discovery, cualquier carpeta raíz fuera de esta lista es identificada como **no-estándar** y debe ser procesada mediante inspección semántica recursiva.

## Directorios Estándar por Framework

| Directorio | Propósito | Frameworks |
|---|---|---|
| `src/` | Código fuente principal | Svelte, React, Vue, Astro |
| `app/` | Rutas y layouts (App Router) | Next.js 13+, SvelteKit |
| `pages/` | Rutas basadas en archivos | Next.js (Pages Router), Astro |
| `components/` | Componentes reutilizables | Todos |
| `lib/` | Utilidades, helpers, stores | Svelte, SvelteKit |
| `public/` | Assets estáticos servidos directamente | Todos |
| `static/` | Assets estáticos (SvelteKit) | SvelteKit |
| `dist/` o `build/` o `.next/` | Salida de compilación (ignorar en discovery) | Todos |
| `node_modules/` | Dependencias (ignorar en discovery) | Todos |
| `test/` o `__tests__/` o `spec/` | Suite de pruebas | Todos |
| `.agents/` | Submódulo oficial de reglas compartidas | Conservar en root |
| `overview/` | Estado local versionado del proyecto | Conservar en root |

## Archivos Estándar en Root

- `package.json`, `package-lock.json`, `pnpm-lock.yaml`, `yarn.lock`
- `vite.config.*`, `svelte.config.*`, `next.config.*`, `astro.config.*`
- `tsconfig.json`, `jsconfig.json`
- `.env`, `.env.local`, `.env.example`
- `README.md`, `LICENSE`, `.gitignore`

## Regla de Inspección para Carpetas No-Estándar

Cualquier otro directorio hallado en el root debe inspeccionarse recursivamente, clasificarse semánticamente según `core/brain.md` y relocalizarse en `overview/`, `overview/context/` o `overview/trackers/`.
