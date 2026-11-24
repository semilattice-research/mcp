# Semilattice MCP

[![Semilattice MCP connector](https://glama.ai/mcp/connectors/io.github.semilattice-research/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.semilattice-research/mcp)

The user simulation layer for agentic marketing, product and design work.
Semilattice gives you and your agents accurate user feedback in minutes, with
state-of-the-art models built from real human data. Fix slop and optimise your work
before users see it.

## What you can ask your agent

- "Come up with a name for our new business account."
- "We have three versions of the free-trial signup. Which one do we ship?"
- "Write the one line under our Pro price that gets free users to upgrade."
- "Write the subject line and opening of the email announcing our new feature."
- "Which launch offer do we run: six months free, £100 to switch, or free international payments?"
- "Set the monthly price for our first paid plan."

The agent writes the work, tests it on simulated users, and fixes what they push back
on. Each answer comes from a user model: a specific target audience, simulated as
hundreds of individual respondents and built from real human data. The first public
user models, US and UK Consumer Finance and US and UK Online Shoppers, are coming
soon, with more to follow.

**Using Claude?** Add the Semilattice plugin from the Claude directory. It bundles this
server with a skill that turns a brief, PRD or spec into tests
([semilattice-research/claude-plugin](https://github.com/semilattice-research/claude-plugin)).

## URL
The Semilattice MCP is a remote server accessible over **Streamable HTTP**. The URL is:

```
https://mcp.semilattice.ai
```
## Connect your client

Step-by-step instructions for Claude, Claude Code, Cursor, ChatGPT, VS Code, Codex,
Gemini CLI, Cline, goose, LibreChat and Cherry Studio are in the docs:
https://docs.semilattice.ai/mcp/connect

Any client that supports remote MCP servers over Streamable HTTP with OAuth should
work. Sign in to your Semilattice account, or create one, with Google, GitHub,
LinkedIn, or email and password.

## Full documentation

[See the full documentation](https://docs.semilattice.ai/mcp/introduction) for information on tools and the Semilattice API.

## Trouble connecting?

As MCP is still a young protocol, clients and servers can sometimes have difficulty connecting. If you're experiencing issues with a specific chatbot, agent platform, or IDE, please email us and we'll be happy to investigate:
```
support@semilattice.ai
```