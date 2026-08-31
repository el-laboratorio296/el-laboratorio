# Release 0.1 — Fundaciones

## Objetivo

Tener una base reproducible para desarrollar EL LABORATORIO sin acoplar la interfaz, la API y la persistencia.

## Entregables

- Monorepo `pnpm` con aplicaciones web y API.
- PostgreSQL definido en Docker Compose.
- Prisma con el modelo de dominio inicial.
- Contrato de salud para verificar la API.
- Guía de ejecución local y variables de entorno de ejemplo.

## Criterios de aceptación

- `pnpm install` resuelve el espacio de trabajo.
- `pnpm lint`, `pnpm typecheck` y `pnpm build` finalizan correctamente.
- `docker compose up --build` expone la web, la API y PostgreSQL.
- `GET http://localhost:3001/health` devuelve el estado de la API.

## Exclusiones

No incluye pagos, autenticación, sorteos en producción ni persistencia de datos reales.
