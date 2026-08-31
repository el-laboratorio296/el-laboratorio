# EL LABORATORIO

Plataforma de rifas con transparencia total. Release 0.1 establece la base técnica: una aplicación web, una API, PostgreSQL y acceso a datos tipado con Prisma.

## Arquitectura

| Componente | Tecnología | Puerto |
| --- | --- | --- |
| `apps/web` | Next.js (App Router) | 3000 |
| `apps/api` | NestJS | 3001 |
| `packages/database` | Prisma + PostgreSQL | 5432 |

## Inicio rápido

1. Instala Node.js 20.9 o superior y Docker Desktop.
2. Copia `.env.example` a `.env`.
3. Ejecuta `pnpm install`.
4. Levanta PostgreSQL: `docker compose up -d postgres`.
5. Aplica la base de datos: `pnpm db:migrate`.
6. Inicia web y API: `pnpm dev`.

También puedes construir los tres servicios con `docker compose up --build`.

## Comprobaciones

```bash
pnpm lint
pnpm typecheck
pnpm build
```

## Alcance de Release 0.1

- Monorepo gestionado con pnpm.
- Página de bienvenida y endpoint `GET /health`.
- Modelo inicial de rifas, premios, boletos y participantes.
- PostgreSQL reproducible mediante Docker Compose.

El siguiente release implementará autenticación, creación de rifas y reserva de boletos.
