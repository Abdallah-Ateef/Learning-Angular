# Figma MCP Integration

This project is configured with the Figma MCP (Model Context Protocol) server, which enables AI agents to work directly with your Figma designs in VS Code.

## Features

- **Get design context**: Extract variables, components, and layout data from Figma designs
- **Generate code from designs**: Select a Figma frame and turn it into Angular code
- **Send UI to Figma**: Capture your live Angular app UI and send it to Figma
- **Write to canvas**: Let AI agents create and modify Figma content directly
- **Code Connect**: Keep generated code consistent with your design components

## Setup

### Prerequisites
- Node.js and npm installed
- Figma account
- VS Code with GitHub Copilot or another MCP-compatible client

### Installation

The Figma MCP is configured in `.vscode/mcp.json`. To activate it:

1. Ensure you have the latest version of `@figma/mcp` installed:
   ```bash
   npm install --save-dev @figma/mcp
   ```

2. The MCP server will be automatically available in your Copilot Chat

### Usage Examples

#### Get Design Context from a Figma File

1. In Figma Design, select the layer you want to get design context for
2. Copy the link to a frame or layer in Figma
3. In VS Code Copilot Chat, paste the URL and ask your AI agent to help implement it

Example prompt:
```
Here's my Figma design: [figma-url]
Please generate Angular components for these UI elements
```

#### Send Your Angular App UI to Figma

Prompt your AI agent:
```
Start a local dev server for my Angular app and capture the UI in a new Figma file
```

The agent will:
1. Start your development server
2. Open a browser window to your app
3. Capture pages and elements as design layers in Figma

#### Generate Code from a Figma Frame

1. Select a Figma frame
2. Prompt your AI agent:
   ```
   Generate Angular TypeScript code for this Figma frame
   ```

## Configuration Files

- `.vscode/mcp.json` - MCP server configuration
- `.vscode/settings.json` - VS Code settings including MCP configuration

## Documentation

For more information about the Figma MCP server:
- [Figma MCP Guide](https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Figma-MCP-server)
- [Remote Server Installation](https://developers.figma.com/docs/figma-mcp-server/remote-server-installation/)
- [Tools and Prompts](https://developers.figma.com/docs/figma-mcp-server/tools-and-prompts/)

## Supported Clients

- VS Code (with GitHub Copilot extension)
- Cursor
- Claude Code
- Codex by OpenAI
- And many others - [See full list](https://www.figma.com/mcp-catalog)

## Plan Requirements

- Remote MCP server: Available on all plans
- Desktop MCP server: Dev or Full seat on paid plans

## Rate Limits

For information about usage and rate limits, see [Plans, access, and permissions](https://developers.figma.com/docs/figma-mcp-server/plans-access-and-permissions/) in the Figma developer documentation.
