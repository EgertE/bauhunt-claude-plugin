# BauHunt for Claude

BauHunt helps builders in Europe turn a construction-material list into a
quote request (requests are sent to suppliers in Estonia today; more countries
follow), keep a future buying wish open and compare supplier offers
including VAT and delivery. Authorized suppliers can prepare offers and browse
open buying wishes.

This plugin contains two things:

- the **BauHunt connector**, a remote MCP server at `https://bauhunt.ee/mcp`;
- the **bauhunt skill**, which tells Claude how to use the connector safely.

## Install

In Claude (web, desktop or Cowork): Customize → Plugins → add BauHunt, then open
the plugin's Connectors tab and sign in with your BauHunt account.

In Claude Code:

```
claude plugin marketplace add EgertE/bauhunt-claude-plugin
claude plugin install bauhunt@bauhunt
```

Then run `/mcp` and sign in to `bauhunt`.

## What to expect

- Public information works without signing in. Your own requests, offers and
  company records need your BauHunt account. Sign-in uses OAuth; the plugin
  holds no passwords or keys.
- Sending a request or an offer always needs your explicit confirmation and the
  current terms.
- BauHunt does not take payments, place binding orders or confirm live stock.
- A submitted request is sent to real suppliers, and their offers come back to
  you. Claude reports the delivery mode the service returns.

## Data

The connector sends what you ask Claude to save or look up (material lists,
delivery location, offers) to BauHunt. See the
[privacy policy](https://bauhunt.ee/privacy) and
[terms](https://bauhunt.ee/terms). Support: https://bauhunt.ee/contact

BauHunt is operated by 24EE OÜ.
