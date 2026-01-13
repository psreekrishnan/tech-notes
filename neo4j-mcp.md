# Neo4j MCP Setup Guide (Windows)

1. Download the MCP binary from the official GitHub release: https://github.com/neo4j/mcp/releases/download/v1.1.1/neo4j-mcp_Windows_x86_64.zip
2. Add MCP Server Entry in `mcp.json` --> C:\Users\%USERNAME%\.aws\amazonq\mcp.json
3. If you've extracted the downloaded  file to c:\Workspace\neo4j-mcp_Windows_x86_64, then you may need to update the command as below,
4. Restart Amazon Q or Reload MCP Config may required.
5. Start prompting from amazonq chat.
```
    Example prompts:

    “Show Neo4j cluster topology”
    “List all nodes and their roles”
```

```
{
  "mcpServers": {
    "neo4j-cp-local-mcp": {
      "command": "C:\\Workspace\\neo4j-mcp_Windows_x86_64\\neo4j-mcp.exe",
      "env": {
        "NEO4J_URI": "bolt://10.54.159.128:61090",
        "NEO4J_USERNAME": "*********",
        "NEO4J_PASSWORD": "***",
        "NEO4J_DATABASE": "neo4j",
        "NEO4J_READ_ONLY": "true"
      },
      "timeout": 60000,
      "disabled": false
    }
  }
}
```
