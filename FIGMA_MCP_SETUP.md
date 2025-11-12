# Figma MCP Server Setup

This project is configured to use the Figma MCP (Model Context Protocol) server with Claude Code.

## Configuration

The Figma MCP server has been configured in Claude Code at `/root/.claude.json`:

```json
"mcpServers": {
  "figma": {
    "url": "https://mcp.figma.com/mcp"
  }
}
```

## What is the Figma MCP Server?

The Figma MCP server allows Claude Code to:
- Access your Figma files and designs
- Generate code from Figma frames
- Extract design context (variables, components, layouts)
- Pull design system information directly into your development workflow

## How to Use

Once configured, you can ask Claude Code to:
- "Generate code from this Figma frame: [URL]"
- "Show me the design variables from my Figma file"
- "Create a component based on this Figma design"

## Server Details

- **Type**: Remote MCP Server
- **URL**: https://mcp.figma.com/mcp
- **Transport**: HTTP
- **Authentication**: Handled through Figma account

## Rate Limits

- **Starter/View/Collab seats**: 6 tool calls per month
- **Dev/Full seats (Professional/Organization/Enterprise)**: Per-minute rate limits (Tier 1 Figma REST API limits)

## Restart Required

After configuration changes, you may need to restart Claude Code for the MCP server to be fully activated.

## Documentation

For more information, visit:
- [Figma MCP Server Guide](https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Figma-MCP-server)
- [Figma Developer Docs](https://developers.figma.com/docs/figma-mcp-server/)
