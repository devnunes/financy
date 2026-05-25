# Financy Web

Frontend application for the Financy project.

---

## 🏁 First Time Setup

If you are new to programming, start from the [main README](../README.md) for a step-by-step guide to running the full project (backend + frontend).

---

## ⚙️ Local Development (Frontend Only)

**Note:** The backend must be running for the frontend to work. See [backend/README.md](../backend/README.md) for backend setup instructions.

1. **Install dependencies**
	```bash
	pnpm install
	```
2. **Start the frontend**
	```bash
	pnpm dev
	```

App: http://localhost:5173

---

## 🔗 Backend Integration

- Apollo Client uses the `VITE_BACKEND_URL` environment variable and sends cookies with `credentials: include`.
- Vite proxies `/graphql` to `http://localhost:3333` during development.

---

## 📂 Project Structure

- `src/pages`: application pages
- `src/router`: routing and route guards
- `src/lib/graphql`: Apollo client, queries, and mutations
- `src/stores`: global state
- `src/components`: reusable components

---

## 🧪 Scripts & Quality

Main scripts:
```bash
# Development
pnpm dev           # start Vite development server
pnpm preview       # preview the production bundle locally

# Build
pnpm build         # run TypeScript build and create production bundle
pnpm build:check   # lint, typecheck, and build in sequence

# Code quality
pnpm lint          # check lint issues with Biome
pnpm format        # format code with Biome
pnpm typecheck     # check TypeScript types
pnpm precommit     # lint, format, and typecheck before commit
```

---

## ✅ Feature Status

- Authentication (login, sign up, session): implemented
- Public and protected routes: implemented
- Authenticated routes: `/dashboard`, `/transactions`, `/categories`, `/profile`
- Dashboard, transactions, and categories: all required features implemented

---

## ⚠️ Note about path alias (@)

The project uses the @ alias for imports from src. Vite resolves this alias automatically, but other environments may not. If you run scripts outside Vite, ensure the environment supports path alias or use relative paths.
