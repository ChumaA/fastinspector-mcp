# FastInspector for Cursor

Ask about your [FastInspector](https://www.fastinspector.com) work in plain language. FastInspector connects real estate agents, home buyers and inspection companies to book and track home inspections.

This plugin adds one remote MCP server, `https://mcp.fastinspector.com`. It contains no code that runs on your machine.

## Before you start

You need:

- A FastInspector account with the current Terms accepted.
- **Allow AI connectors (MCP)** turned on in FastInspector settings. It's off by default. An inspector's company owner must turn it on too.

## Setup

1. Install the plugin.
2. Open the `fastinspector` MCP server in Cursor and sign in with your FastInspector account.

There's no API key to set. Sign-in uses OAuth, and you can disconnect at any time by turning **Allow AI connectors (MCP)** off.

## Tools

All eight tools are read-only.

| Tool | Who can use it | What it does |
|---|---|---|
| `get_me` | Everyone | Shows your profile and company |
| `list_notifications` | Everyone | Lists your notifications |
| `list_my_bookings` | Agents and buyers | Lists your bookings |
| `get_booking` | Agents and buyers | Shows one booking's details |
| `list_inspection_types` | Agents and buyers | Lists inspection types |
| `list_eligible_companies` | Agents and buyers | Finds companies that can inspect a property |
| `list_company_requests` | Inspection companies | Lists your company's requests and jobs |
| `list_my_appointments` | Inspectors | Lists your assigned appointments |

Other roles get a clear error from a tool that isn't for them.

## Try asking

- "Which of my inspections are coming up, and what's their status?"
- "Show the details and contingency deadline for my latest booking."
- "Which companies can do a general inspection at this property?"
- "What new requests does my company have?"
- "What's on my inspection schedule this week?"

## Data and privacy

The connector signs in as you and sees only what your account can already see. It can't book, accept, pay, sign or change anything. It doesn't return inspection reports, findings or photos, card or bank details, or share links.

- [Setup guide](https://www.fastinspector.com/blog/ai-connectors)
- [Privacy Policy](https://www.fastinspector.com/privacy)
- Support: support@fastinspector.com

## License

MIT, see [LICENSE](LICENSE). The FastInspector name and logo aren't covered by that license.
