# GraphQL API Explorer

A lightweight browser-based GraphQL schema explorer built with React, Vite, and GraphQL Voyager. It renders a schema visualization from GraphQL SDL and is designed for quickly exploring complex GraphQL APIs without running a dedicated GraphQL UI server.

## Features

- Visualize GraphQL schemas as interactive relationship diagrams
- Load schema definitions directly from SDL text
- Hide deprecated fields and sort fields alphabetically for cleaner exploration
- Built with Vite for a fast local development workflow
- Works directly in the browser using the bundled schema proxy

## Tech Stack

- React 18
- TypeScript
- Vite
- GraphQL.js
- GraphQL Voyager

## Requirements

- Node.js >= 18
- pnpm >= 8

## Quick Start

1. Install dependencies:
   ```bash
   pnpm install
   ```

2. Start the development server:
   ```bash
   pnpm serve
   ```

3. Open the app in your browser at the local Vite URL (typically http://localhost:8085).

## Production Build

```bash
pnpm build
```

The build output is generated into the `dist/` directory.

## Project Structure

```text
src/
  App.tsx          # Main GraphQL Voyager integration
  App.scss         # Custom styling overrides
  main.tsx         # App bootstrap
  utils/
    sdl-to-introspection.ts # SDL validation and schema conversion helper
```

## Notes

This project reads a schema from `@threatmap/schema-proxy/graphql?raw` and converts SDL to an introspection-compatible object before rendering. That allows the explorer to visualize schema relationships without needing a live GraphQL endpoint.
