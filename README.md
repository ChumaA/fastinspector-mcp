# FastInspector MCP connector

Connects AI assistants to [FastInspector](https://www.fastinspector.com) over the [Model Context Protocol](https://modelcontextprotocol.io). FastInspector connects real estate agents, home buyers and inspection companies to book and track home inspections. Ask about your bookings, company requests, appointments and notifications in plain language.

| | |
|---|---|
| **Server URL** | `https://mcp.fastinspector.com` |
| **Transport** | Streamable HTTP (remote; nothing to install or run locally) |
| **Auth** | OAuth with your FastInspector account (no API key) |
| **Access** | Read-only (`fastinspector.read` scope) |

## Requirements

- A FastInspector account with the current Terms accepted.
- **Allow AI connectors (MCP)** turned on in FastInspector settings. It's off by default. An inspector's company owner must turn it on too.

Each person signs in as themselves, so the assistant sees only what that person can already see in FastInspector.

## Connect

- **Claude:** open [FastInspector in the Claude directory](https://claude.ai/directory/fastinspector) and choose **Connect to Claude**.
- **Claude Code:** run `claude mcp add --transport http fastinspector https://mcp.fastinspector.com`.
- **Cursor:** install the plugin, or add the server to your MCP settings using this repo's [`mcp.json`](mcp.json).
- **ChatGPT:** in ChatGPT, open **Plugins → Add → Add custom MCP server** and enter the server URL with OAuth. The OpenAI plugin package (listing for ChatGPT and Codex) is in [`openai/`](openai).
- **Grok:** ask a Grok Bot in a chat to add the connector, and give it the server URL.

The server only admits approved clients, so another MCP client may be refused. To ask for one to be added, email support@fastinspector.com.

On first use your client opens a FastInspector sign-in page and asks you to allow access. Turn **Allow AI connectors (MCP)** off at any time to disconnect.

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

## Limits

Up to 60 tool calls per minute and 1,000 per day per person, and 300 per minute per company. Every call is logged for security and kept for 12 months.

## Links

- Setup guide: <https://www.fastinspector.com/blog/ai-connectors>
- Privacy Policy: <https://www.fastinspector.com/privacy>
- Terms of Service: <https://www.fastinspector.com/terms>
- Support: support@fastinspector.com · <https://www.fastinspector.com/contact>

Reviewers: a test account with sample data is available on request at support@fastinspector.com.

## License

MIT, see [LICENSE](LICENSE). The FastInspector name and logo aren't covered by that license.
