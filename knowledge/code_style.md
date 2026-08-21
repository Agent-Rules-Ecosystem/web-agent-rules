# Estilo y Convenciones de Código Web

## Nomenclatura

| Elemento | Convención | Ejemplo |
|---|---|---|
| Componentes | `PascalCase` | `UserProfileCard.svelte` |
| Archivos de utilidad | `camelCase` o `kebab-case` | `authUtils.ts` / `auth-utils.ts` |
| Variables / funciones | `camelCase` | `fetchUserData()` |
| Constantes | `UPPER_SNAKE_CASE` | `MAX_RETRIES` |
| CSS clases | `kebab-case` | `.user-profile-card` |
| Stores / Composables | `camelCase` con prefijo descriptivo | `useAuthStore`, `authStore` |

## TypeScript

- Preferir `interface` sobre `type` para formas de objetos públicas.
- No usar `any` salvo en casos extremos justificados con comentario.
- Activar `strict: true` en `tsconfig.json`.
- Props de componentes con tipos explícitos siempre.

## Async / Manejo de Errores

- Preferir `async/await` sobre `.then()` encadenado.
- Nunca silenciar errores con `catch(e) {}` vacío.
- Separar errores de red, validación y negocio en capas distintas.
- Usar loading/error states explícitos en la UI.

## Organización

- Archivos idealmente < 250 líneas; máximo 300.
- Un componente por archivo.
- Separar lógica de negocio de la capa de presentación (stores/composables/hooks vs componentes).
- No mezclar estilos de navegación en el mismo proyecto.
