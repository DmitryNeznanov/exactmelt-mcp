# ExactMelt MCP app

ExactMelt values metals and coins inside ChatGPT, Claude and other MCP
clients. Enter weight, purity, quantity or rolls, compare a buyer's offer,
exchange gold and silver, or build a mixed worksheet. Every result links to a
prefilled PDF report on [exactmelt.com](https://exactmelt.com).

- Website: https://exactmelt.com
- Documentation: https://exactmelt.com/app
- Privacy: https://exactmelt.com/privacy
- Terms: https://exactmelt.com/terms

This repository documents the hosted connector. It does not contain the
website or its code.

## Connect

- Endpoint: `https://exactmelt.com/api/mcp`
- Transport: Streamable HTTP
- Authentication: none (no account, sign-in or API key)

```json
{ "mcpServers": { "exactmelt": { "url": "https://exactmelt.com/api/mcp" } } }
```

In ChatGPT, add it as a custom app/connector with no authentication. In
Claude, open Customize → Connectors → Add custom connector and enter the URL.

## Tools

All tools are read-only.

| Tool | What it does |
|---|---|
| `calculate_melt_value` | Precious-metal melt value, fine content, unit rates and an optional buyer-offer comparison |
| `calculate_coin_value` | Coin melt value and fine-metal content by quantity, standard rolls or measured grams |
| `find_coins` | Coin presets with issue years, specifications and current melt value per coin |
| `get_coin` | One coin preset with its specifications and a quantity-one melt calculation |
| `calculate_exchange` | Gold-to-silver or silver-to-gold exchange weight at current quotes |
| `calculate_penny_nickel` | Penny or nickel alloy metal value at the base-metal prices you enter |

## Try asking

- "What's my 14K ring worth, 5.2 grams?"
- "Calculate the melt value of 10 Morgan dollars."
- "Exchange 1 troy ounce of gold for silver at current spot."

## Report an issue

Open an issue in this repository or email abishop1933@gmail.com.

## License

The documentation files in this repository are MIT licensed (see
[LICENSE](LICENSE)). The ExactMelt website, its content, data and brand are
not covered by this license.
