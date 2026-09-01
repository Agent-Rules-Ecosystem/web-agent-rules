# Checklist pre-release Web

Cuando el usuario pida desplegar, construir bundle de producción (`npm run build`) o auditar la versión Web: ejecutar checklist, mostrar comandos; no ejecutar build de producción sin solicitud explícita.

- [ ] Linter y TypeScript sin errores (`npm run lint`, `npx tsc`).
- [ ] Suite de pruebas verde (`npm test`), si hay tests.
- [ ] Sin `console.log()` olvidados en código de producción.
- [ ] Variables de entorno `.env` de producción configuradas y auditadas.
- [ ] `overview/trackers/progress.md` y tracker correspondiente actualizados.

## Production Build

```bash
npm run build
```

## Preview Local

```bash
npm run preview
```
