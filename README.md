# ☕ Caffeine Website

> A full-stack website built with Caffeine on the Internet Computer Protocol (ICP).

This repository contains the source code for a decentralized website managed by **Caffeine**. It features a modern frontend interface seamlessly connected to a backend canister, fully containerized for easy deployment.

## 🏗️ Architecture

- **Framework:** Managed via `caffeine.toml` which defines the `frontend` website and its `backend` dependencies.
- **Backend:** Motoko-based smart contracts utilizing the `mops` package manager.
- **Frontend:** TypeScript website managed via `pnpm`.
- **Integration:** Uses automated bindings (`pnpm bindgen`) to ensure type-safe RPC calls from the frontend to the backend.

## 🚀 Quick Start (Docker)

The easiest way to build and serve the website is via the included Docker configuration:

```bash
docker build -t app .
docker run -it --network host app
```

## 💻 Local Development

If you prefer to run the environment locally without Docker, follow these steps:

### 1. Backend (Motoko)
From the `src/backend/` directory:
```bash
mops install
mops check --fix
mops build
```

### 2. Integration (Bindings)
From the root directory, generate the type bindings so the website can communicate with the backend:
```bash
pnpm bindgen
```

### 3. Frontend Website
From the `src/frontend/` directory:
```bash
pnpm install --prefer-offline
pnpm build
```

## 📖 Design System
See `DESIGN.md` for architectural design principles and `AGENTS.md` for CLI command references.