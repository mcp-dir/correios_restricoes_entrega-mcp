# Instalação rápida

Correios: Entrega Diferenciada é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_correios_restricoes_entrega`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Correios: Entrega Diferenciada` / `https://api.mcp.ai/p_correios_restricoes_entrega`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "correios_restricoes_entrega": { "type": "http", "url": "https://api.mcp.ai/p_correios_restricoes_entrega" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=correios_restricoes_entrega&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jb3JyZWlvc19yZXN0cmljb2VzX2VudHJlZ2EifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "correios_restricoes_entrega": { "url": "https://api.mcp.ai/p_correios_restricoes_entrega" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=correios_restricoes_entrega&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_correios_restricoes_entrega%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "correios_restricoes_entrega": { "type": "http", "url": "https://api.mcp.ai/p_correios_restricoes_entrega" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_correios_restricoes_entrega
```

Dúvidas? [correios_restricoes_entrega@mcp.ai](mailto:correios_restricoes_entrega@mcp.ai)
