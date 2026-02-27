# Setup

## Repository Setup

Go to the root of your repository.

### [opensrc](https://github.com/vercel-labs/opensrc#readme)

Fetch source code for npm packages to give coding agents deeper context than types alone.

```sh
# Install opensrc globally
npm install -g opensrc

# Fetch source code for packages used in the project
opensrc react react-dom react-error-boundary tailwindcss tailwind-variants tw-animate-css zod zustand @testing-library/react @testing-library/jest-dom @testing-library/user-event
```

### [Repomix](https://github.com/yamadashy/repomix#readme)

Repomix is a powerful tool that packs your entire repository into a single, AI-friendly file.
It is perfect for when you need to feed your codebase to Large Language Models (LLMs).

```sh
npx repomix apps/app-name -o repomix/repomix-app-name.xml
```

### [Preflight](https://github.com/preflightsh/preflight#readme)

Preflight is a Go-based CLI tool that scans a codebase and related configuration for launch readiness.

```sh
npm install -g @preflightsh/preflight
preflight init
```
