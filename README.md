# Pathrule

Pathrule is the shared memory, rules, and skills layer for AI coding agents.

Use the CLI to connect a local repository to Pathrule, sync the workspace
context agents need, and install Pathrule into tools such as Claude Code,
Cursor, Codex, and Windsurf.

## Getting Started

Install the CLI:

```bash
npm i -g @pathrule/cli
```

Run setup from the repository you want to connect:

```bash
cd your-project
pathrule setup
```

`pathrule setup` guides you through sign-in when needed, finds or creates the
right workspace, attaches the current folder, syncs local companion files, and
offers to install Pathrule for your AI tools.

## What Pathrule Gives Your Agents

- Path-scoped context, delivered just in time instead of pasted into every chat.
- Shared memory, rules, and skills that survive between AI sessions.
- One workspace layer for Claude Code, Cursor, Codex, Windsurf, and other
  MCP-compatible tools.
- Local setup for companion files, MCP config, SSH sessions, and headless
  terminals.
- A privacy-first model: Pathrule does not read, scan, or upload your source
  code.

## Common Commands

```bash
pathrule setup
pathrule sync
pathrule start
pathrule status
```

For diagnostics:

```bash
pathrule doctor
```

For scripted setup:

```bash
pathrule setup --json
pathrule setup --workspace <workspace-id-or-name> --target all --yes
```

## Install Options

### npm

```bash
npm i -g @pathrule/cli
```

Upgrade:

```bash
npm i -g @pathrule/cli@latest
```

### Homebrew

```bash
brew install sertanhelvaci/tap/pathrule
```

Upgrade:

```bash
brew upgrade sertanhelvaci/tap/pathrule
```

## Authentication

Most users do not need to run `pathrule login` manually. `pathrule setup`
starts the hosted Pathrule authorization flow when the CLI is not signed in.

You can still sign in directly:

```bash
pathrule login
```

The login flow shows a one-time code and opens Pathrule Web in your browser.

## Security

Pathrule is designed for team workspaces without taking custody of your
repository:

- Your source code stays on your machine.
- Cloud access uses user sessions, not embedded service keys.
- Workspace permissions are enforced server-side and by database row-level
  security.
- The local bridge binds to loopback and is intended for local browser and CLI
  workflows only.

For more details, visit [pathrule.io](https://pathrule.io).
