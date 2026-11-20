# ATS New Job Postings Monitor — Greenhouse, Lever & Ashby — MCP Server

Watch Greenhouse, Lever and Ashby job boards from your AI agent or MCP client and get only the postings you have not seen before — company, title, location, department, team, employment type, posted date, job and apply URLs, as clean structured records. A one-shot fetch of a board's current postings is also available when an agent just needs the latest listings now, and monitoring mode on a schedule turns the same boards into a quiet new-posting alert feed.

This repo is the MCP listing for the [ATS New Job Postings Monitor — Greenhouse, Lever & Ashby](https://apify.com/magnova/ats-new-postings-monitor) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--ats-new-postings-monitor** — Monitor Greenhouse, Lever and Ashby job boards for new postings, or fetch a board's current postings in one shot. Returns structured records: company, title, location, department, team, employment type, posted date, job and apply URLs.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/ats-new-postings-monitor
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "ats-new-postings-monitor": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/ats-new-postings-monitor"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "ats-new-postings-monitor": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/ats-new-postings-monitor"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/ats-new-postings-monitor-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.01 per posting returned — $10 per 1,000 postings**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/ats-new-postings-monitor
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/ats-new-postings-monitor

*Posting records come from the boards' own public listings — no API key needed.*
