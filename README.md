# Stocklake MCP — AI Stock Intelligence

Real-time and historical US/international stock market data, technical indicators, AI-synthesized research, insider/institutional activity, and macro/sector intelligence — delivered over the [Model Context Protocol](https://modelcontextprotocol.io).

**MCP endpoint:** `https://api.stocklake.dev/mcp`
**Docs:** [stocklake.dev/docs](https://stocklake.dev/docs)
**Register:** [stocklake.dev/register](https://stocklake.dev/register)

---

## Quickstart — OAuth (Claude, ChatGPT, Perplexity)

1. Add MCP server `https://api.stocklake.dev/mcp` in your client (Claude.ai → Settings → Connectors; ChatGPT → Settings → Connectors → Developer Mode; Perplexity Pro/Max/Enterprise → Developer Mode → remote connector)
2. Complete the OAuth flow — no key to copy
3. Ask about any stock

Any other MCP client that speaks OAuth (Cursor, Windsurf, VS Code, Zed, etc.) works the same way via Dynamic Client Registration — no server-side setup needed on our end.

## Quickstart — API key

```bash
# Get a free key at https://stocklake.dev/register
curl -X POST https://api.stocklake.dev/mcp \
  -H "Authorization: Bearer sl_your_key" \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"get_stock","arguments":{"symbol":"AAPL"}}}'
```

---

## Tools

Free and guest tiers share the same 8 tools — Pro unlocks extra fields on these plus 9 additional AI-research tools. 17 tools total.

| Tool | Tier | Description |
|------|------|-------------|
| `get_stock` | free | Price, fundamentals, indicators — Pro adds AI rating, per-indicator signals, relative-strength |
| `get_stocks` | free | Batch version of `get_stock`, up to 25 symbols |
| `get_stock_history` | free | Daily OHLCV |
| `get_stock_news` | free | Headlines — Pro adds full AI sentiment/impact/flag-score fields |
| `get_screener` | free | Fundamentals + technicals filter/rank, up to 25/call — Pro adds high-conviction preset |
| `get_market_movers` | free | Top gainers/losers/most active |
| `get_market_pulse` | free | VIX, Fear & Greed, market breadth |
| `get_earnings_calendar` | free | Upcoming earnings dates |
| `get_stock_research` | pro | Full per-symbol deep dive: AI summary, news, insider activity, live signal |
| `get_insider_activity` | pro | Insider + institutional sentiment |
| `get_indicator_history` | pro | Up to 730 days of daily indicator snapshots |
| `get_signals` | pro | Live AI-scored signal queue |
| `get_news_feed` | pro | Market-wide AI news briefing |
| `get_market_assessment` | pro | Macro regime + market outlook |
| `get_sector_intelligence` | pro | AI sector signals for all 11 GICS sectors, incl. rotation view |
| `get_earnings_intelligence` | pro | Post-earnings AI verdicts and risk flags |
| `get_watchlist` | pro | Account-scoped saved symbols with live AI verdicts |

---

## Tiers

| Tier | Calls/day | Auth |
|------|-----------|------|
| Guest | 25 | No key — IP-rate-limited |
| Free | 200 | API key, no expiry |
| Pro | 5000 | API key or OAuth — $20.00/month |

Free keys issued instantly at [stocklake.dev/register](https://stocklake.dev/register). No credit card.

---

## Transport

- **Protocol:** MCP Streamable HTTP
- **Endpoint:** `https://api.stocklake.dev/mcp`
- **Auth:** `Authorization: Bearer <key>` / `X-API-Key: <key>`, or OAuth 2.1 with PKCE (Dynamic Client Registration supported — any OAuth-capable MCP client can self-register)
- **Registry:** `dev.stocklake/stocklake` on the [MCP Registry](https://registry.modelcontextprotocol.io)

---

## Links

- [Documentation](https://stocklake.dev/docs)
- [Register for free key](https://stocklake.dev/register)
- [Dashboard](https://stocklake.dev/dashboard)
- [Legal / Privacy](https://stocklake.dev/legal)
- [Contact](https://stocklake.dev/contact)
