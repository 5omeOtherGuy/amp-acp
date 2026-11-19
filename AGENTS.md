# AGENTS.md

## Commands
- `bun run build` — Bundle TypeScript to `dist/index.js` (single file, Bun target)
- `bun start` or `bun dist/index.js` — Run the ACP adapter
- `bun run lint` — Type-check with `tsc --noEmit`
- `bun test src/` — Run tests with Bun's built-in test runner
- `bun run test:e2e:live` — Full-stack opt-in verification (binary + fake-CLI e2e + real Amp CLI + orb execution); needs an authenticated Amp CLI, consumes real Amp usage

## Rules
- stdout is for the ACP protocol only: log with `console.error`.

## Update Protocol

Canonical documentation:

- `README.md` — Installation, configuration, user-facing capabilities, architecture and code style
- `AGENTS.md` — Development commands and repository rules
- `docs/mcp-passthrough.md` — MCP configuration behavior and troubleshooting
- `docs/npm-oidc-trusted-publishing.md` — npm publishing and release authentication

| Change type | README | README architecture list | Specialized docs |
|---|---:|---:|---:|
| User-facing capability | Yes | Maybe | Maybe |
| Architecture or state change | Yes | Yes | Maybe |
| MCP behavior | Yes | Maybe | `docs/mcp-passthrough.md` |
| Release or publishing | Maybe | No | `docs/npm-oidc-trusted-publishing.md` |
| Rename or removal | Yes | Yes | Affected docs |
