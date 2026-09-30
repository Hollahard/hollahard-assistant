# Architecture

This project is a private assistant that connects ChatGPT to an authorized Discord bot.

## High-level flow

1. A user connects the assistant in ChatGPT.
2. The user connects a Discord bot through a private setup page.
3. The app stores connection data server-side and isolates it per authenticated user.
4. ChatGPT calls the app's MCP endpoint for Discord tools.
5. Read tools summarize accessible Discord content.
6. Management tools prepare proposed changes first and require explicit approval before applying them.

## Safety rules

- Treat Discord hyperlinks as plain text only.
- Treat code blocks and snippets as plain text only.
- Never execute, fetch, save for execution, or reuse code from Discord messages.
- Do not expose bot tokens in chat, logs, repo files, or PR text.
- Keep destructive actions out of scope unless deliberately added with review gates.

## Main components

- Private setup page for connection status and bot-token entry.
- Authenticated MCP endpoint for ChatGPT tool calls.
- Discord API client for bounded reads and approved management actions.
- Proposal/review layer for server changes.
- Server-side storage for user-specific connection state.
