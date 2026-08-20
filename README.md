# 🌐 ICP Web3 Starter

> A full-stack decentralized application built for the Internet Computer Protocol (ICP).

This repository contains a full-stack Web3 application utilizing a **Motoko** backend canister and a modern **TypeScript/PNPM** frontend. It includes a complete Dockerized build pipeline and automated binding generation for seamless frontend-to-backend communication.

## 🏗️ Architecture

- **Backend:** Built with Motoko, utilizing the `mops` package manager.
- **Frontend:** Built with TypeScript, managed via `pnpm`.
- **Integration:** Uses automated bindings (`pnpm bindgen`) to ensure type-safe RPC calls from the frontend to the Motoko canister.

## 🚀 Quick Start (Docker)

The easiest way to run the application is via the included Docker configuration:

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
From the root directory, generate the type bindings so the frontend can communicate with the backend:
```bash
pnpm bindgen
```

### 3. Frontend
From the `src/frontend/` directory:
```bash
pnpm install --prefer-offline
pnpm build
```

## 📖 Design System
See `DESIGN.md` for architectural design principles and `AGENTS.md` for CLI command references.