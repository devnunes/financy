# Financy

<p align="center">
	<b>Full-stack financial management app</b><br>
	<i>Built as a final postgraduate project at Rocketseat Faculty of Technology</i>
	<img src="./frontend/screenshot/dashboard.png" alt="Dashboard Screenshot">
</p>

---

## 🚀 Quick Start (First Run)

Follow these steps to get the project running locally for the first time:

### 1. Prerequisites

- [Node.js 20+](https://nodejs.org/)
- [pnpm](https://pnpm.io/)
- [Git](https://git-scm.com/)

### 2. Clone the repository

```bash
git clone <repo-url>
cd financy
```

### 3. Install monorepo dependencies

```bash
# In the root folder
pnpm install
```

### 4. Setup backend

```bash
cd backend 
```

- Environment variables

```bash
cp .env.example .env.dev
# Edit .env.dev if needed (see backend/README.md for required variables)
```

- Install dependencies

```bash
# In backend
pnpm install
```

- Run the backend

```bash
pnpm dev:db   # generate Prisma client, create/apply migrations, and seed the database
pnpm dev            # start the backend server
```

Backend GraphQL API: http://localhost:3333/graphql

### 5. Setup frontend

```bash
cd frontend
```

- Setup environment variables

```bash
cp .env.example .env.dev
# Edit .env.dev if needed (see frontend/README.md for frontend variables)
```

- Install dependencies

```bash
# In frontend
pnpm install
```

- Run the frontend

```bash
pnpm dev
```

Frontend app: http://localhost:5173

### 6. Demo User (Seed)

After running the seed, you can log in with this demo user:

#### Email:
```text
seeduser@example.com
```
#### Password: 
```text
hashedpassword
```

*If you change the seed, update the password above accordingly.*

> The seed script automatically creates this user to make testing and validation easier.

---

## 📁 Monorepo Structure

- `backend`: GraphQL API (Fastify, Apollo Server, TypeGraphQL, Prisma)
- `frontend`: React + Vite web client (Apollo Client)

See each folder's README for more details and advanced usage.

---

## 🛠️ Main Technologies

- Backend: Node.js, TypeScript, Fastify, Apollo Server, TypeGraphQL, Prisma, SQLite, Vitest
- Frontend: React 19, TypeScript, Vite, Apollo Client, React Hook Form, Zod, Zustand, Tailwind CSS
- Quality: Biome, Vitest

---

## ✅ Challenge Requirements Status

- Account creation and sign in: implemented
- User can manage only their own transactions: implemented
- User can manage only their own categories: implemented
- Create transaction: implemented
- Delete transaction: implemented
- Edit transaction: implemented
- List transactions: implemented
- Create category: implemented
- Delete category: implemented
- Edit category: implemented
- List categories: implemented

---






## Tests and Quality

- Backend tests: `pnpm test`, `pnpm test:watch`, `pnpm test:coverage`
- Frontend quality checks: `pnpm lint`, `pnpm check:biome`, `pnpm build`

## Notes

- Backend GraphQL schema is generated from registered resolvers.
- Frontend authentication flow and route protection are available.
- Dashboard, transactions, and categories UX in the frontend are under active iteration.

## ℹ️ More Info

- Backend setup, environment variables, and scripts: [backend/README.md](./backend/README.md)
- Frontend setup, scripts, and structure: [frontend/README.md](./frontend/README.md)