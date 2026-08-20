# ☕ Caffeine Website

> A full-stack website built with Caffeine on the Internet Computer Protocol (ICP).

**Note:** This repository is presented as an architectural reference for full-stack canister development on the Internet Computer. 

This project contains the source code for a decentralized website managed by **Caffeine**. It features a modern frontend interface seamlessly connected to a backend canister, fully containerized for scalable deployment.

## 🏗️ Architecture

- **Framework:** Managed via `caffeine.toml` which defines the `frontend` website and its `backend` dependencies within a unified workspace.
- **Backend:** Motoko-based smart contracts utilizing the `mops` package manager to handle decentralized state and logic.
- **Frontend:** TypeScript website managed via `pnpm`, delivering a modern, responsive user experience.
- **Integration:** Uses automated bindings (`pnpm bindgen`) to ensure type-safe RPC calls from the frontend to the backend canister, virtually eliminating serialization errors.

## 📖 Design System
See `DESIGN.md` for architectural design principles and `AGENTS.md` for legacy CLI command references.