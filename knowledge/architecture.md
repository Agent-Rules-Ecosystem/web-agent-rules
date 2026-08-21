# Arquitectura de Proyectos Web

## Capas de Arquitectura

| Capa | Responsabilidad | Ejemplos |
|---|---|---|
| **Presentación** | Renderizado de UI, interacción del usuario | Componentes, páginas, layouts |
| **Estado / Lógica** | Manejo de estado, lógica de negocio frontend | Stores (Svelte), Context/Hooks (React), Composables (Vue) |
| **Servicios** | Comunicación con APIs externas y backend | Fetch wrappers, API clients, WebSocket handlers |
| **Persistencia** | Almacenamiento local del cliente | localStorage, IndexedDB, cookies |

## Patrones Recomendados

- **Componentes presentacionales vs contenedores**: Separar UI pura de lógica con estado.
- **Colocation**: Mantener styles, tests y lógica cerca del componente que los usa.
- **Single Responsibility**: Cada módulo/componente hace una sola cosa bien.
- **Barrel exports** (`index.ts`): Para simplificar imports en módulos grandes.

## Reglas de Arquitectura

- Nunca importar directamente entre módulos de dominio cruzado sin pasar por la capa de servicios.
- Los componentes no llaman directamente a APIs HTTP — eso es responsabilidad de los servicios/stores.
- El estado global solo para datos verdaderamente compartidos; preferir estado local cuando sea posible.
