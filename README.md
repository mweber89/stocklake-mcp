# Stocklake MCP — AI Stock Intelligence

Real-time stock prices, fundamentals, technical indicators, AI-analysed news, macro regime, and sector intelligence — delivered over the [Model Context Protocol](https://modelcontextprotocol.io).

**MCP endpoint:** `https://api.stocklake.dev/mcp`  
**Docs:** [stocklake.dev/docs](https://stocklake.dev/docs)  
**Register:** [stocklake.dev/register](https://stocklake.dev/register)

---

## Quickstart — Claude.ai

1. Open Claude.ai → Settings → Integrations
2. Add MCP server: `https://api.stocklake.dev/mcp`
3. Complete the OAuth flow
4. Done — ask Claude about any stock

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

| Tool | Tier | Description |
|------|------|-------------|
| `get_stock` | guest | Price, fundamentals, technical indicators |
| `get_stocks` | free | Batch data for up to 10 symbols |
| `get_stock_history` | free | Daily OHLCV up to 365 days |
| `get_company_profile` | free | Sector, industry, description, employees, financials |
| `search_stocks` | free | Filter by sector, country, RSI signal, recommendation |
| `get_earnings_calendar` | free | Upcoming earnings dates |
| `get_stock_rating` | pro | AI technical rating 0–10 (RSI, MACD, Bollinger, SMA) |
| `get_stock_news` | pro | AI-analysed news with sentiment and flag score |
| `get_sentiment_profile` | pro | Insider + institutional sentiment (SEC Form 4, Nasdaq) |
| `get_macro_regime` | pro | AI macro regime with FRED indicators, VIX, Fear & Greed |
| `get_market_outlook` | pro | BULLISH/NEUTRAL/BEARISH outlook with preferred sectors |
| `get_sector_intelligence` | pro | AI sector signals for all 11 GICS sectors |

---

## Tiers

| Tier | Calls/day | Auth |
|------|-----------|------|
| Guest | 500 | No key — IP-rate-limited |
| Free | 500 | API key (30-day, renewable) |
| Pro | 5000 | API key or OAuth — $19.99/month |

Free keys issued instantly at [stocklake.dev/register](https://stocklake.dev/register). No credit card.

---

## Transport

- **Protocol:** MCP Streamable HTTP (`2025-11-25`)
- **Endpoint:** `https://api.stocklake.dev/mcp`
- **Auth:** `Authorization: Bearer <key>` or OAuth 2.1 (Claude.ai)
- **Registry:** `dev.stocklake/stocklake` on the [MCP Registry](https://registry.modelcontextprotocol.io)

---

## Links

- [Documentation](https://stocklake.dev/docs)
- [Register for free key](https://stocklake.dev/register)
- [Dashboard](https://stocklake.dev/dashboard)
- [Legal / Privacy](https://stocklake.dev/legal)
- [Contact](https://stocklake.dev/contact)
