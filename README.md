# Andru for Claude and Cursor

Andru is an enterprise buyer specialist for complex B2B deals. This plugin gives Claude or Cursor one skill that tells it when to use Andru and which tool fits each question, and connects it to Andru's hosted server.

## What's in it

- **A skill** (`skills/andru/SKILL.md`): when to use Andru, which tool answers which question, when to ask the person before a paid call, and how long to wait on longer jobs.
- **A connector**: Andru's hosted MCP server. Claude reads `.mcp.json` (`https://mcp.andru-ai.com/mcp`); Cursor uses the address in `.cursor-plugin/plugin.json` (`https://mcp.andru-ai.com/mcp?signin=first`), which asks you to sign in before connecting.
- **Two manifests**: `.claude-plugin/plugin.json` for Claude and `.cursor-plugin/plugin.json` for Cursor.

There is no code in this plugin: no scripts, no hooks, no local server, and nothing installed on your computer.

## What it connects to and sends

- Claude connects to `https://mcp.andru-ai.com/mcp` and Cursor to `https://mcp.andru-ai.com/mcp?signin=first`. You sign in with your Andru account through Andru's sign-in page at `https://api.andru-ai.com`; no key is stored in the plugin.
- When Claude or Cursor uses a tool, it sends Andru what that tool needs: company websites and names, buyer titles, deal details, and your email if you sign up from the chat.
- Andru answers from your Andru account. Nothing is sent anywhere else, and the plugin reads no files on your computer.

## What it costs

Lookups are free. Some tools draw on your prepaid Andru wallet and are charged only when they deliver. The skill tells Claude or Cursor to ask you before it uses them, and the spending limit you set caps what it can spend. See https://andru-ai.com/pricing.

## Use it

- In Claude, add the plugin, then connect Andru from the plugin's Connectors tab and sign in.
- In Claude Code, the skill and the server load with the plugin; run `/mcp` to sign in.
- In Cursor, install the plugin from **Customize**, then sign in when Cursor asks the first time a tool needs your account.

## Links

- Set-up: https://andru-ai.com/docs/mcp
- Privacy: https://andru-ai.com/privacy
- Terms: https://andru-ai.com/terms
- Support: https://andru-ai.com/support or geter@andru-ai.com

## License

MIT
