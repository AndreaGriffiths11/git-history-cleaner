# Contributing to Git History Cleaner

Thank you for your interest in contributing! This document explains how to set up a local development environment, the project conventions, and how to submit changes.

## Table of Contents

- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Project Structure](#project-structure)
- [Code Style](#code-style)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Reporting Bugs](#reporting-bugs)
- [Requesting Features](#requesting-features)

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 20 or higher
- npm (comes with Node.js)
- Git

### Local Setup

```bash
# 1. Fork the repository on GitHub, then clone your fork
git clone https://github.com/<your-username>/git-history-cleaner.git
cd git-history-cleaner

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev
```

The app will be available at `http://localhost:5173`.

## Development Workflow

| Command | Description |
|---|---|
| `npm run dev` | Start the Vite dev server with hot-reload |
| `npm run build` | Type-check and build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint across all source files |

Before opening a pull request, make sure all of the following pass locally:

```bash
npm run lint
npm run build
```

## Project Structure

```
git-history-cleaner/
├── src/
│   ├── App.tsx              # Root component — main UI and script generation logic
│   ├── ErrorFallback.tsx    # Error boundary fallback UI
│   ├── main.tsx             # React entry point
│   ├── index.css            # Global styles and CSS custom properties
│   ├── components/
│   │   └── ui/              # Reusable shadcn/ui-based components
│   ├── hooks/               # Custom React hooks
│   ├── lib/                 # Shared utility functions
│   └── styles/              # Additional style modules
├── public/                  # Static assets served as-is
├── index.html               # HTML entry point
├── vite.config.ts           # Vite configuration
├── tailwind.config.js       # Tailwind CSS configuration
└── tsconfig.json            # TypeScript configuration
```

### Key Source Files

- **`src/App.tsx`** — Contains the form, script-generation logic, and command explanations. Most feature work happens here.
- **`src/components/ui/`** — Primitive UI components built on [Radix UI](https://www.radix-ui.com/) and styled with Tailwind CSS. These are generally not modified directly; prefer composing them in `App.tsx` or new feature components.

## Code Style

- **TypeScript** — All new code should be written in TypeScript with proper typing. Avoid `any`.
- **Functional components** — Use React functional components and hooks; no class components.
- **Tailwind CSS** — Use Tailwind utility classes for styling. Avoid inline `style` props.
- **Formatting** — The project uses ESLint (`npm run lint`). Fix all lint errors before opening a PR.
- **Comments** — Keep comments minimal and purposeful. Self-documenting code is preferred.

## Submitting a Pull Request

1. **Create a branch** from `main` with a descriptive name:
   ```bash
   git checkout -b feat/my-new-feature
   # or
   git checkout -b fix/issue-description
   ```

2. **Make your changes** and commit with clear, concise messages:
   ```bash
   git commit -m "feat: add confirmation dialog before script download"
   ```

3. **Run checks** before pushing:
   ```bash
   npm run lint && npm run build
   ```

4. **Push your branch** and open a pull request against `main`:
   ```bash
   git push origin feat/my-new-feature
   ```

5. In the PR description, explain:
   - **What** the change does
   - **Why** it is needed
   - Any relevant screenshots or recordings for UI changes

Pull requests are reviewed on a best-effort basis. Small, focused PRs are merged much faster than large ones.

## Reporting Bugs

Please [open a GitHub issue](https://github.com/AndreaGriffiths11/git-history-cleaner/issues/new) and include:

- A clear description of the bug
- Steps to reproduce
- Expected vs. actual behavior
- Browser and OS information
- Any relevant screenshots or console errors

> For security vulnerabilities, please follow the process described in [SECURITY.md](SECURITY.md) rather than opening a public issue.

## Requesting Features

[Open a GitHub issue](https://github.com/AndreaGriffiths11/git-history-cleaner/issues/new) with:

- A description of the feature and the problem it solves
- Any relevant examples or mockups

---

Thank you for helping improve Git History Cleaner! 🧹
