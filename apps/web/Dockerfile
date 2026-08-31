FROM node:24-alpine AS base
WORKDIR /app
RUN corepack enable
COPY package.json pnpm-workspace.yaml pnpm-lock.yaml tsconfig.base.json ./
COPY apps/web/package.json apps/web/package.json
COPY apps/api/package.json apps/api/package.json
COPY packages/database/package.json packages/database/package.json
RUN pnpm install --frozen-lockfile
COPY . .
RUN pnpm --filter @el-laboratorio/web build
EXPOSE 3000
CMD ["pnpm", "--filter", "@el-laboratorio/web", "start"]
