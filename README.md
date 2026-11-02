# Emailchaser cold email for Cursor

Run cold email campaigns from Cursor through the Emailchaser remote MCP server: 102 tools for campaigns, sequences, leads and the Lead Finder database, replies and AI reply drafts, sender mailboxes, warmup, inbox placement and Autopilot.

- **Server:** `https://app.emailchaser.com/api/mcp` (streamable HTTP, listed in the official MCP registry as `com.emailchaser/emailchaser`)
- **Website:** [emailchaser.com/mcp-server](https://www.emailchaser.com/mcp-server)

## Set your API key

Create an API key in the Emailchaser app under **API & MCP** (a read-only key works for reports; a read and write key runs campaigns), then make it available to Cursor as an environment variable:

```bash
export EMAILCHASER_API_KEY="your key"
```

`mcp.json` reads it with `${env:EMAILCHASER_API_KEY}`, so the key never sits in a file.

## What is inside

- `mcp.json`: connects Cursor to the server with your key.
- `rules/emailchaser.mdc`: tells the agent to work through Emailchaser and to ask before sending or spending credits.
- `skills/launch-a-cold-email-campaign`: from a company website to a launched campaign.
- `skills/fix-deliverability`: find why emails land in spam and fix it.
- `skills/handle-replies`: triage replies, edit and send AI drafts, record meetings.

## Install by hand

Add this to `.cursor/mcp.json` in your project or to your global Cursor settings:

```json
{
  "mcpServers": {
    "emailchaser": {
      "url": "https://app.emailchaser.com/api/mcp",
      "headers": {
        "Authorization": "Bearer ${env:EMAILCHASER_API_KEY}"
      }
    }
  }
}
```

## License

MIT
