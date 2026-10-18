# CreceRank MCP

Remote MCP server for AI visibility (GEO) in Latin America and Spain.

CreceRank measures whether ChatGPT, Gemini, AI Overviews, and Perplexity recommend your brand. After you connect your CreceRank account, an agent can read visibility, cited sources, and GEO actions, save prompts, and start a scan. The same plan limits as the app apply. There is a 14-day trial, with no credit card.

This repository documents the hosted server. The CreceRank application source is not published here.

## Endpoint

| | |
| --- | --- |
| URL | `https://crecerank.onrender.com/mcp` |
| Transport | Streamable HTTP |
| Auth | OAuth 2.1 with PKCE (S256) |

Sign in with Google or email, the same login as the app. Do not put tokens in the URL. There is no npm package and no PyPI package.

## Connect

### Cursor

```json
{
  "mcpServers": {
    "crecerank": {
      "url": "https://crecerank.onrender.com/mcp"
    }
  }
}
```

### Claude Code

```bash
claude mcp add --transport http crecerank https://crecerank.onrender.com/mcp
```

### Claude Desktop and ChatGPT

Paste `https://crecerank.onrender.com/mcp` as a remote connector and finish OAuth in the browser.

Guided install: <https://app.crecerank.com/integrations/mcp/agents>

## What an agent can do

- Read the account, brands, visibility, cited sources, and recommendations
- Create a brand, save prompts, and start a scan
- Share a brand with a teammate

Deletes (a brand, a scan, or a member) need the extra scope `mcp.destructive`. That scope stays off unless you check it on the consent screen.

The server does not delete the account, start a Google Analytics connection, or take payment.

## Scopes

- `mcp.read` and `mcp.write` by default
- `mcp.destructive` only if you allow it on the consent screen

Tool catalog: <https://app.crecerank.com/integrations/mcp/docs>

## Links

- Product: <https://crecerank.com/>
- Landing: <https://app.crecerank.com/integrations/mcp>
- Privacy: <https://crecerank.com/politicas-de-privacidad/>
- Support: hola@rankerstudio.com

## En español

CreceRank ayuda a medir y mejorar tu ranking en las IAs. El servidor remoto usa la misma cuenta que la app. Tienes 14 días de prueba, sin tarjeta.

## License

Proprietary. This repository only documents the hosted CreceRank MCP server.
