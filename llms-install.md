# Installing the QuoteBill MCP server

QuoteBill is a remote MCP server. There is nothing to download, build or configure beyond its address, and it needs no API key. It is for QuoteBill members: the first time you connect, your client opens QuoteBill in the browser, where you sign in (or sign up free, Google works) and choose Allow. The client discovers this sign-in from the server's 401 answer (OAuth 2.1, dynamic client registration).

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
