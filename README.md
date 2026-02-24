# Claude Code Config

Personal Claude Code setup — commands, skills, and MCP config templates.

## Structure

```
commands/       # Custom slash commands
  codex.md      # /codex — hand off tasks to OpenAI Codex CLI
mcp-servers.example.json  # MCP server config template (no secrets)
```

## MCP Servers

Active servers (configured in `~/.claude.json` via `claude mcp add --scope user`):

| Server | Package | Purpose |
|--------|---------|---------|
| `exa` | `exa-mcp-server` | AI-powered web search |
| `github` | `@modelcontextprotocol/server-github` | GitHub issues, PRs, repos |

To set up on a new machine:
```bash
claude mcp add --scope user exa -- npx -y exa-mcp-server
claude mcp add --scope user github -- npx -y @modelcontextprotocol/server-github
```

Then add your API keys via `claude mcp edit` or directly in `~/.claude.json`.
See `mcp-servers.example.json` for the expected structure.

## Custom Commands

### `/codex [task]`
Hands off a task to the OpenAI Codex CLI agent non-interactively.

```
/codex refactor the auth module to use async/await
/codex write unit tests for UserService
```

Requires [Codex CLI](https://github.com/openai/codex) installed (`npm i -g @openai/codex`).

## Setup on a New Machine

```bash
# Clone into ~/.claude
git clone https://github.com/soumyyy/claudecode-config.git ~/.claude

# Add MCP servers (fill in your own keys)
claude mcp add --scope user exa -- npx -y exa-mcp-server
claude mcp add --scope user github -- npx -y @modelcontextprotocol/server-github
```
