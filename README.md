# Panel de Automatizaciones — Módulo Contable

Panel web para visualizar el estado de los casos de prueba automatizados del Sprint Automation Contable + los bugs encontrados en Sprint 5.

## Fuentes de datos

- **Automatizaciones** → lista ClickUp `901326925580` (Sprint Automation Contable)
- **Bugs** → lista ClickUp `901326731539` (Sprint 5 Módulo Contable)

Los datos se consumen vía el Cloudflare Worker `panel-bugs-proxy` que inyecta el token de ClickUp.

## Funcionalidad

- Agrupación por **Sección → Flujo** (parseo del título `Modulo Contable - <Sección> - <Flujo>`).
- Contadores por flujo: `testing pass` / `testing fail` / `pendiente` / `done` + barra de progreso.
- Pestaña **Bugs Encontrados**: bugs del Sprint 5 separados en *En desarrollo*, *A testear / QA* y *Cerrados*.
- Auto-refresh cada 5 minutos (nuevos casos se suman solos).
- Exportar PDF con resumen por flujo + detalle de casos.

## Publicación

GitHub Pages desde la rama `main`, raíz del repo.
