# Financy

Aplicação FullStack de gerenciamento financeiro desenvolvida como **trabalho final de pós-graduação na Faculdade de Tecnologia Rocketseat**.

## Sobre o desafio

O Financy tem como objetivo permitir que cada usuário organize suas finanças com autenticação, transações e categorias.

### Requisitos do desafio

- [x] O usuário pode criar uma conta e fazer login
- [x] O usuário pode ver e gerenciar apenas as transações criadas por ele
- [ ] O usuário pode ver e gerenciar apenas as categorias criadas por ele *(camada de resolver/serviço existe no backend, integração GraphQL pública ainda pendente)*
- [x] Deve ser possível criar uma transação
- [x] Deve ser possível deletar uma transação
- [x] Deve ser possível editar uma transação
- [x] Deve ser possível listar todas as transações
- [ ] Deve ser possível criar uma categoria *(implementado no resolver/serviço; falta registro no schema publicado)*
- [ ] Deve ser possível deletar uma categoria *(implementado no resolver/serviço; falta registro no schema publicado)*
- [ ] Deve ser possível editar uma categoria *(implementado no resolver/serviço; falta registro no schema publicado)*
- [ ] Deve ser possível listar todas as categorias *(implementado no resolver/serviço; falta registro no schema publicado)*

## Estrutura dos projetos

Este workspace usa submódulos Git:

- `financy-server`: API GraphQL com Fastify + Apollo + TypeGraphQL + Prisma
- `financy-web`: aplicação web React + Vite + Apollo Client

## Tecnologias principais

- **Backend:** Node.js, TypeScript, Fastify, Apollo Server, TypeGraphQL, Prisma, SQLite, Vitest
- **Frontend:** React 19, TypeScript, Vite, Apollo Client, React Hook Form, Zod, Zustand, Tailwind CSS
- **Qualidade:** Biome, Vitest

## Como executar o projeto completo

### 1) Backend

```bash
cd financy-server
pnpm install
cp .env.example .env.dev # se existir
pnpm dev
```

Servidor GraphQL disponível em `http://localhost:3333/graphql`.

### 2) Frontend

```bash
cd financy-web
pnpm install
pnpm dev
```

Aplicação web disponível em `http://localhost:5173`.

## Observações importantes

- O backend possui cobertura de testes para serviços, resolvers e middleware de autenticação.
- O frontend já possui fluxo de autenticação e proteção de rotas.
- As páginas de dashboard, transações e categorias no frontend ainda estão em evolução de interface e integração completa.
