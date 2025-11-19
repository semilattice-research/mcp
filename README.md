# Semilattice MCP

Semilattice gives agents the ability to predict how specific audiences answer questions. Use it to test content, personalise features, and A/B test decisions.

![Screenshot of an LLM interface with the user asking the LLM to use Semilattice to predict "if developers foresee AGI in the next 10 years". The LLM uses the Semilattice MCP to "list population models", finds a Developer audience model, and then proceeds to use that model to predict the answer to the user's question.](mcp.png)

## URL
The Semilattice MCP is a remote server accessible over **Streamable HTTP**. The URL is:

```
https://mcp.semilattice.ai
```
## Full documentation

[See the full documentation](https://docs.semilattice.ai/mcp/introduction) for information on tools and the Semilattice API.

## Client-specific instructions

> **Note:** This list is not exhaustive. Semilattice MCP should work with any client which supports connecting to remote MCP servers over Streamable HTTP with OAuth.

### ChatGPT web

**Prerequisites**: paid ChatGPT subscription

1. Navigate to **Settings** from the account menu (bottom left corner)
2. Click **Apps & Connectors** in left-side nav
3. Click **Advanced Settings** at bottom of tab
4. Toggle on **Developer Mode**
5. Go back to **Apps & Connectors** tab
6. Click **Create** in top right of the Connectors section
7. Add a descriptive name like `semilattice` in the **name** field. Optionally add a short explanation
8. Enter `https://mcp.semilattice.ai` as the **MCP Server URL**
9. Leave the authentication toggle default "OAuth"
10. Tick the warning box for **Custom MCPs**
11. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with ChatGPT!

**Known issue:** ChatGPT cannot execute multiple tool calls in parallel or sequentially. You have to ask every question separately or prompt ChatGPT to continue the process after every question if it has planned to predict multiple questions.

### Claude Code

1. In a CLI where you have Claude Code installed, before running Claude Code itself, run:
```bash
claude mcp add --transport http semilattice https://mcp.semilattice.ai
```
2. Start Claude Code with `claude`
3. Run `/mcp` to list MCPs. You should see `semilattice △ disconnected · Enter to login`
4. Select the Semilattice MCP and hit Enter
5. Select the `Authenticate` option on the next screen
6. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with Claude Code!

See the [Claude Code docs](https://code.claude.com/docs/en/mcp) for more info.

### Claude desktop

**Prerequisites**: paid Claude subscription

1. Navigate to **Settings** from the account menu (bottom left corner)
2. Click **Add custom connector** below the list of Connectors
3. Add a descriptive name e.g. `semilattice`
4. Enter the MCP URL: `https://mcp.semilattice.ai`
5. Leave advanced settings blank
6. Click **Connect**
7. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with Claude!

### Claude web

**Prerequisites**: paid Claude subscription

1. Navigate to **Settings** from the account menu (bottom left corner)
2. Click **Add custom connector** below the list of Connectors
3. Add a descriptive name e.g. `semilattice`
4. Enter the MCP URL: `https://mcp.semilattice.ai`
5. Leave "Advanced settings" blank
6. Click **Connect**
7. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with Claude!

### Cline

1. Open the Cline plugin in your IDE
2. Find and click the **MCP Servers** button to open the MCP Servers menu
3. Select the **Configure** tab and click **Configure MCP Servers**
4. The `cline_mcp_settings.json` file will open in the editor. Update it to add Semilattice MCP:
```json
{
    "mcpServers": {
        "semilattice": {
            "type": "streamableHttp",
            "url": "https://mcp.semilattice.ai"
        }
    }
}
```

5. Save the file and Semilattice MCP should appear in the Cline plugin interface
6. Click **Authenticate** in the Cline interface
7. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with Cline!

### Cursor

1. Click [this link](cursor://anysphere.cursor-deeplink/mcp/install?name=semilattice&config=eyJ1cmwiOiJodHRwczovL21jcC5zZW1pbGF0dGljZS5haSJ9) to add Semilattice MCP to Cursor
2. In Cursor, click **Install** to confirm adding Semilattice MCP
3. Click **Connect** to authenticate
4. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with Cursor!

The above process will add the Semilattice MCP to your `mcp.json` file. You can also skip the steps above and edit this directly:
```json
{
    "mcpServers": {
        "semilattice": {
            "url": "https://mcp.semilattice.ai",
            "headers": {}
        }
    }
}
```

See the [Cursor docs](https://cursor.com/docs/context/mcp) for more info.

### Gemini CLI

1. Open your `settings.json` file, usually found at `~/.gemini/settings.json`
2. Add Semilattice MCP:
```json
{
    ...other config
    "mcpServers": {
        "semilattice": {
            "httpUrl": "https://mcp.semilattice.ai"
        }
    }
}
```

3. Start or restart Gemini CLI with `gemini`
4. Authentication should be triggered automatically, if not run `/mcp auth semilattice`
5. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with Gemini CLI!

See the [Gemini CLI docs](https://geminicli.com/docs/tools/mcp-server/) for more info.

### goose

1. Select **Extensions** from the left-nav
2. Click **Add custom extension**
3. Enter a descriptive name like `semilattice`
4. Select **Streamable HTTP** from the **Type** dropdown
5. Enter the Semilattice MCP URL in the **Endpoint** field:
```
https://mcp.semilattice.ai
```

6. Leave other fields blank and click **Add Extension**
7. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with goose!

### LibreChat

1. Update your `librechat.yaml` file to add Semilattice MCP:
```yaml
mcpServers:
  semilattice:
    type: streamable-http
    url: https://mcp.semilattice.ai
    requiresOAuth: true
```

2. In LibreChat, click the MCP dropdown in the main prompt input field
3. Click the 🔑 key icon next to Semilattice
4. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with LibreChat!

See the [LibreChat docs](https://www.librechat.ai/docs/features/mcp) for more info.

### VS Code

1. Open the VSCode command palette: `Shift` + `Command` + `P` (Mac) or `Ctrl` + `Shift` + `P` (Windows/Linux)
2. Type "mcp" and select the **MCP: Add Server...** action
3. Select the **HTTP (HTTP or Server-Sent Events)** option
4. Enter the Semilattice MCP URL: `https://mcp.semilattice.ai`
5. Enter "semilattice" or another descriptive name when prompted for a Server ID
6. Choose whether to add the MCP globally or just to the current workspace
7. Go through the authentication flow to create or sign into a Semilattice account with your Google email

🎉 Semilattice should now be ready to use with VS Code!

The above process will add the Semilattice MCP to your `mcp.json` file. You can also skip the steps above and edit this directly:
```json
{
    "servers": {
        "semilattice": {
            "url": "https://mcp.semilattice.ai",
            "type": "http"
        }
    },
    "inputs": []
}
```

See the [VS Code docs](https://code.visualstudio.com/docs/copilot/customization/mcp-servers) for more info.

## Trouble connecting?

As MCP is still a young protocol, clients and servers can sometimes have difficulty connecting. If you're experiencing issues with a specific chatbot, agent platform, or IDE, please email us and we'll be happy to investigate:
```
support@semilattice.ai
```