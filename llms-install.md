# Installing the QuoteBill MCP server

QuoteBill is a remote MCP server. There is nothing to download, build or configure beyond its address, and it needs no API key or sign-in.

Add this server to the MCP settings:

```json
{
  "mcpServers": {
    "quotebill": {
      "url": "https://quotebill.com/mcp",
      "type": "streamableHttp"
    }
  }
}
```

Check it works by calling `get_tax_rule` with `{ "country": "KR" }`: the answer names VAT with a rate of 0.1 (10%) and its official source.
