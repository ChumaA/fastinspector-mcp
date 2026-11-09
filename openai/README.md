# OpenAI plugin package

The FastInspector listing for OpenAI's plugin directory (ChatGPT and Codex), in the Agent Plugins format: `plugin.json`, `mcp.json` and `assets/`. It is kept apart from the Cursor plugin at the repo root because both formats use a root `mcp.json`.

Build the ZIP from inside this folder, so `plugin.json` sits at the archive root:

```bash
cd openai && zip -r -X ../fastinspector-openai-plugin.zip plugin.json mcp.json assets -x '*.DS_Store'
```

Sign-in uses OAuth with CIMD (ChatGPT's published client identity); no client secret goes in the package. Reviewer credentials, test cases and the demo video go in the OpenAI dashboard, not here.
