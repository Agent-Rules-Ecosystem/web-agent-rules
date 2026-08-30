# 🌐 Web Agent Rules

**Cerebro operativo centralizado para agentes de IA en proyectos Web**. Cubre desarrollo con Svelte, React, Vue, Astro, Three.js, WebSockets y stacks frontend/fullstack modernos.

Se instala como submódulo de Git en `.agents/`. Las reglas globales son 100% agnósticas e independientes del código fuente del proyecto.

---

## 📌 Pilares de Gobernanza

1. **⚡ Modo Cavernícola & Token Saver**: Respuestas ultra-concisas, eliminación de prosa innecesaria y referencias de líneas en lugar de duplicación de código.
2. **🔄 Sincronización Automática de Rastreadores**: Actualización simultánea e integral de los archivos de control en `overview/` durante `$work` y `$close`.
3. **🗺️ Arquitectura Viva (`$archi`)**: Mantenimiento incremental del mapa técnico en `overview/architecture.md` mediante diagramas Mermaid sintéticos.
4. **👥 Handoff y Memoria Versionada por Agente**: Firma canónica por proveedor/modelo. Historial incremental de soluciones y traspaso transparente al cambiar de agente.
5. **🛡️ Escudo Anti-parches (Filtro Agnóstico)**: Las mejoras al core prohiben código específico o comandos CLI rígidos.
6. **🔒 Inviolabilidad de `.agents/`**: Los archivos de gobernanza nunca se modifican desde el proyecto local.

---

## ⚡ $-Comandos

| Comando | Descripción |
|---|---|
| `$boot` | Bootstrap completo, lectura de reglas, verificación de `overview/` y handoff de agente. |
| `$status` | Muestra el estado activo en 5 líneas. |
| `$work [descripción]` | Registra tarea/bug y sincroniza todos los rastreadores. |
| `$archi` | Escanea cambios estructurales y actualiza diagramas Mermaid en `overview/architecture.md` (Hub) y `overview/architecture/` (Spoke). |
| `$learn [texto]` | Valida con Filtro Agnóstico y registra propuesta candidata. |
| `$learnagnostico [texto]` | Descontextualiza entidades de negocio y registra en `overview/learning.md`. |
| `$close` | Cierre de sesión, validación de calidad y sincronización final. |

---

## 📦 Instalación

```bash
git submodule add https://github.com/xolotl-hub/web-agent-rules.git .agents
```

Copiar el adaptador correspondiente desde `.agents/adapters/` según la herramienta de IA utilizada.

Iniciar con: `$boot`
