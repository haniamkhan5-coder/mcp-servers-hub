<p align="center">
  <img src="https://img.shields.io/badge/MCP-Servers Hub-00B4D8?style=for-the-badge" alt="MCP Servers" />
  <img src="https://img.shields.io/badge/Servers-50+-blueviolet?style=for-the-badge" alt="50+ Servers" />
  <img src="https://img.shields.io/badge/Install_Guides-Included-brightgreen?style=for-the-badge" alt="Install Guides" />
  <img src="https://img.shields.io/badge/PRs-Welcome-orange?style=for-the-badge" alt="PRs Welcome" />
  <img src="https://img.shields.io/badge/License-CC0%201.0-lightgrey?style=for-the-badge" alt="License" />
</p>

<h1 align="center">🔌 MCP Servers Hub</h1>

<p align="center">
  <strong>50+ Verified MCP Servers with Install Guides & Config Snippets</strong>
  <br />
  <em>Connect your AI agents to databases, APIs, tools & services — in seconds</em>
</p>

<p align="center">
  <a href="https://aiagentbase.app/skills">🚀 Deploy on AiAgentBase</a> •
  <a href="#-how-to-contribute">🤝 Contribute</a> •
  <a href="#-quick-start">⚡ Quick Start</a> •
  <a href="https://modelcontextprotocol.io">📋 MCP Spec</a>
</p>

---

> 🚀 **Deploy MCP Servers in 1-Click!** Visit [AiAgentBase.app](https://aiagentbase.app/skills) — The Community-Driven AI Skills & Tools Marketplace

---

## 📖 What is MCP?

**Model Context Protocol (MCP)** is an open standard by **Anthropic** that enables AI agents to connect with external tools, databases, and APIs. Think of MCP servers as the **hands and feet** of your AI — while [Agent Skills](https://agentskills.io) are the **brain**.

```
Skills (SKILL.md) = AI's BRAIN  (knowledge, rules, expertise)
MCP Servers       = AI's HANDS  (actions, tools, integrations)
```

---

## ⚡ Quick Start

Add any MCP server to your AI tool by editing the config file:

**Claude Desktop:** `claude_desktop_config.json`
**Cursor:** `.cursor/mcp.json`
**Windsurf:** MCP settings panel

```json
{
  "mcpServers": {
    "server-name": {
      "command": "npx",
      "args": ["-y", "@package/mcp-server"],
      "env": {
        "API_KEY": "your-key-here"
      }
    }
  }
}
```

---

## 📂 Catalog — 50+ Verified MCP Servers

### 🗄️ Databases (10 servers)

#### 1. PostgreSQL MCP — *by Anthropic (Official)*
> Query & manage PostgreSQL databases with schema inspection
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres", "postgresql://user:pass@localhost:5432/mydb"]
    }
  }
}
```

---

#### 2. SQLite MCP — *by Anthropic (Official)*
> Local SQLite database operations & business intelligence
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "sqlite": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sqlite", "/path/to/database.db"]
    }
  }
}
```

---

#### 3. MongoDB MCP — *by MongoDB, Inc.*
> MongoDB Atlas & local database queries, collections, schema inspection
> 
> 🔗 [GitHub](https://github.com/mongodb-js/mongodb-mcp-server) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "mongodb": {
      "command": "npx",
      "args": ["-y", "mongodb-mcp-server"],
      "env": {
        "MDB_MCP_CONNECTION_STRING": "mongodb+srv://user:pass@cluster.mongodb.net/mydb"
      }
    }
  }
}
```

---

#### 4. MySQL MCP — *by designcomputer*
> MySQL database integration with secure query execution
> 
> 🔗 [GitHub](https://github.com/designcomputer/mysql_mcp_server) · 🐍 Python

```json
{
  "mcpServers": {
    "mysql": {
      "command": "uvx",
      "args": ["mysql-mcp-server"],
      "env": {
        "MYSQL_HOST": "localhost",
        "MYSQL_PORT": "3306",
        "MYSQL_USER": "root",
        "MYSQL_PASSWORD": "your-password",
        "MYSQL_DATABASE": "mydb"
      }
    }
  }
}
```

---

#### 5. Supabase MCP — *by Supabase, Inc.*
> Full Supabase platform — auth, database, storage, edge functions, migrations
> 
> 🔗 [GitHub](https://github.com/supabase/mcp) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "supabase": {
      "command": "npx",
      "args": ["-y", "@supabase/mcp-server"],
      "env": {
        "SUPABASE_ACCESS_TOKEN": "your-access-token"
      }
    }
  }
}
```

---

#### 6. Redis MCP — *by Redis, Inc.*
> Redis cache, data store, vector search & session management
> 
> 🔗 [GitHub](https://github.com/redis/mcp-redis) · 🐍 Python · 🎖️ Official

```json
{
  "mcpServers": {
    "redis": {
      "command": "uvx",
      "args": ["mcp-redis"],
      "env": {
        "REDIS_URL": "redis://localhost:6379"
      }
    }
  }
}
```

---

#### 7. Neon MCP — *by Neon, Inc.*
> Serverless Postgres with database branching & management
> 
> 🔗 [GitHub](https://github.com/neondatabase/mcp-server-neon) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "neon": {
      "command": "npx",
      "args": ["-y", "@neondatabase/mcp-server-neon"],
      "env": {
        "NEON_API_KEY": "your-neon-api-key"
      }
    }
  }
}
```

---

#### 8. ClickHouse MCP — *by ClickHouse, Inc.*
> ClickHouse analytical database — schema inspection & queries
> 
> 🔗 [GitHub](https://github.com/ClickHouse/mcp-clickhouse) · 🐍 Python · 🎖️ Official

```json
{
  "mcpServers": {
    "clickhouse": {
      "command": "uvx",
      "args": ["mcp-clickhouse"],
      "env": {
        "CLICKHOUSE_HOST": "localhost",
        "CLICKHOUSE_PORT": "8123",
        "CLICKHOUSE_USER": "default",
        "CLICKHOUSE_PASSWORD": "your-password"
      }
    }
  }
}
```

---

#### 9. Turso MCP — *by Turso (ChiselStrike)*
> Edge SQLite database powered by libSQL
> 
> 🔗 [GitHub](https://github.com/turso-extended/mcp-server-turso) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "turso": {
      "command": "npx",
      "args": ["-y", "@turso/mcp-server"],
      "env": {
        "TURSO_AUTH_TOKEN": "your-token",
        "TURSO_URL": "libsql://your-db.turso.io"
      }
    }
  }
}
```

---

#### 10. CockroachDB MCP — *by amineelkouhen*
> Distributed SQL database — management, monitoring & querying
> 
> 🔗 [GitHub](https://github.com/amineelkouhen/mcp-cockroachdb) · 🐍 Python

```json
{
  "mcpServers": {
    "cockroachdb": {
      "command": "uvx",
      "args": ["mcp-cockroachdb"],
      "env": {
        "DATABASE_URL": "postgresql://user:pass@localhost:26257/defaultdb"
      }
    }
  }
}
```

---

### 🌐 Web & Browser Automation (8 servers)

#### 11. Puppeteer MCP — *by Anthropic (Official)*
> Browser automation, web scraping & screenshot capture
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/puppeteer) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "puppeteer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-puppeteer"]
    }
  }
}
```

---

#### 12. Playwright MCP — *by Microsoft*
> Cross-browser automation using accessibility tree
> 
> 🔗 [GitHub](https://github.com/microsoft/playwright-mcp) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-server-playwright"]
    }
  }
}
```

---

#### 13. Brave Search MCP — *by Anthropic (Official)*
> Web & local search via Brave Search API
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "brave-search": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-brave-search"],
      "env": {
        "BRAVE_API_KEY": "your-brave-api-key"
      }
    }
  }
}
```

---

#### 14. Firecrawl MCP — *by Mendable/Firecrawl*
> Advanced web scraping, crawling & content extraction
> 
> 🔗 [GitHub](https://github.com/mendableai/firecrawl-mcp-server) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "npx",
      "args": ["-y", "firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "your-firecrawl-key"
      }
    }
  }
}
```

---

#### 15. Browserbase MCP — *by Browserbase*
> Cloud browser infrastructure — headless automation at scale
> 
> 🔗 [GitHub](https://github.com/browserbase/mcp-server-browserbase) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "browserbase": {
      "command": "npx",
      "args": ["-y", "@browserbasehq/mcp-server"],
      "env": {
        "BROWSERBASE_API_KEY": "your-api-key",
        "BROWSERBASE_PROJECT_ID": "your-project-id"
      }
    }
  }
}
```

---

#### 16. Fetch MCP — *by Anthropic (Official)*
> Fetch web content and convert to markdown
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "fetch": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fetch"]
    }
  }
}
```

---

#### 17. EXA MCP — *by EXA AI*
> AI-native web search with semantic understanding
> 
> 🔗 [GitHub](https://github.com/exa-labs/exa-mcp-server) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "exa": {
      "command": "npx",
      "args": ["-y", "exa-mcp-server"],
      "env": {
        "EXA_API_KEY": "your-exa-key"
      }
    }
  }
}
```

---

#### 18. Tavily MCP — *by Tavily*
> AI search engine optimized for LLMs and RAG
> 
> 🔗 [GitHub](https://github.com/tavily-ai/tavily-mcp) · 🐍 Python · 🎖️ Official

```json
{
  "mcpServers": {
    "tavily": {
      "command": "uvx",
      "args": ["tavily-mcp"],
      "env": {
        "TAVILY_API_KEY": "your-tavily-key"
      }
    }
  }
}
```

---

### 🛠️ Developer Tools (10 servers)

#### 19. GitHub MCP — *by GitHub / Microsoft*
> Repos, issues, PRs, actions, code search & management
> 
> 🔗 [GitHub](https://github.com/github/github-mcp-server) · 🏎️ Go · 🎖️ Official

```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@anthropic/github-mcp-server"],
      "env": {
        "GITHUB_TOKEN": "your-github-pat"
      }
    }
  }
}
```

---

#### 20. GitLab MCP — *by GitLab*
> Projects, merge requests, CI/CD pipelines & issues
> 
> 🔗 [GitLab](https://gitlab.com/gitlab-org/editor-extensions/gitlab-mcp-server) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "gitlab": {
      "command": "npx",
      "args": ["-y", "@anthropic/gitlab-mcp-server"],
      "env": {
        "GITLAB_TOKEN": "your-gitlab-token",
        "GITLAB_URL": "https://gitlab.com"
      }
    }
  }
}
```

---

#### 21. Docker MCP — *by Docker, Inc.*
> Container management, image operations & orchestration
> 
> 🔗 [GitHub](https://github.com/docker/docker-mcp) · 🏎️ Go · 🎖️ Official

```json
{
  "mcpServers": {
    "docker": {
      "command": "docker",
      "args": ["mcp", "serve"]
    }
  }
}
```

---

#### 22. Sentry MCP — *by Sentry*
> Error tracking, performance monitoring & issue management
> 
> 🔗 [GitHub](https://github.com/getsentry/sentry-mcp) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "sentry": {
      "command": "npx",
      "args": ["-y", "@sentry/mcp-server"],
      "env": {
        "SENTRY_AUTH_TOKEN": "your-sentry-token"
      }
    }
  }
}
```

---

#### 23. Linear MCP — *by Linear*
> Issue tracking, project management & team workflows
> 
> 🔗 [GitHub](https://github.com/linearapp/linear-mcp-server) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "linear": {
      "command": "npx",
      "args": ["-y", "@anthropic/linear-mcp-server"],
      "env": {
        "LINEAR_API_KEY": "your-linear-key"
      }
    }
  }
}
```

---

#### 24. Figma MCP — *by Figma Context*
> Access Figma design files, components & styles
> 
> 🔗 [GitHub](https://github.com/nickarora/figma-context-mcp) · 📇 TypeScript

```json
{
  "mcpServers": {
    "figma": {
      "command": "npx",
      "args": ["-y", "figma-context-mcp"],
      "env": {
        "FIGMA_API_KEY": "your-figma-key"
      }
    }
  }
}
```

---

#### 25. Postman MCP — *by Postman*
> API testing, collections & workspace management
> 
> 🔗 [GitHub](https://github.com/nickarora/postman-mcp-server) · 📇 TypeScript

```json
{
  "mcpServers": {
    "postman": {
      "command": "npx",
      "args": ["-y", "@nickarora/postman-mcp-server"],
      "env": {
        "POSTMAN_API_KEY": "your-postman-key"
      }
    }
  }
}
```

---

#### 26. Cloudflare MCP — *by Cloudflare*
> Workers, KV, R2, D1 database & Cloudflare services
> 
> 🔗 [GitHub](https://github.com/cloudflare/mcp-server-cloudflare) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "cloudflare": {
      "command": "npx",
      "args": ["-y", "@cloudflare/mcp-server-cloudflare"],
      "env": {
        "CLOUDFLARE_API_TOKEN": "your-cf-token",
        "CLOUDFLARE_ACCOUNT_ID": "your-account-id"
      }
    }
  }
}
```

---

#### 27. Vercel MCP — *by Vercel*
> Deployments, domains, projects & serverless functions
> 
> 🔗 [GitHub](https://github.com/vercel/vercel-mcp) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "vercel": {
      "command": "npx",
      "args": ["-y", "@vercel/mcp"],
      "env": {
        "VERCEL_TOKEN": "your-vercel-token"
      }
    }
  }
}
```

---

#### 28. Netlify MCP — *by Netlify*
> Site deployments, forms & serverless functions
> 
> 🔗 [GitHub](https://github.com/netlify/mcp-server-netlify) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "netlify": {
      "command": "npx",
      "args": ["-y", "@anthropic/netlify-mcp-server"],
      "env": {
        "NETLIFY_AUTH_TOKEN": "your-netlify-token"
      }
    }
  }
}
```

---

### 📈 Business & Productivity (8 servers)

#### 29. Slack MCP — *by Anthropic (Official)*
> Messages, channels, users & workspace management
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "slack": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-slack"],
      "env": {
        "SLACK_BOT_TOKEN": "xoxb-your-bot-token",
        "SLACK_TEAM_ID": "T0123456789"
      }
    }
  }
}
```

---

#### 30. Notion MCP — *by Notion*
> Pages, databases, blocks & workspace management
> 
> 🔗 [GitHub](https://github.com/makenotion/notion-mcp-server) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "notion": {
      "command": "npx",
      "args": ["-y", "@notionhq/notion-mcp-server"],
      "env": {
        "NOTION_API_KEY": "ntn_your-notion-key",
        "OPENAPI_MCP_HEADERS": "{\"Authorization\": \"Bearer ntn_your-notion-key\", \"Notion-Version\": \"2022-06-28\"}"
      }
    }
  }
}
```

---

#### 31. Google Drive MCP — *by Anthropic (Official)*
> File access, search & management in Google Drive
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "gdrive": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-gdrive"],
      "env": {
        "GDRIVE_CREDENTIALS": "/path/to/credentials.json"
      }
    }
  }
}
```

---

#### 32. Google Maps MCP — *by Anthropic (Official)*
> Geocoding, directions, places & distance matrix API
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/google-maps) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "google-maps": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-google-maps"],
      "env": {
        "GOOGLE_MAPS_API_KEY": "your-google-maps-key"
      }
    }
  }
}
```

---

#### 33. Todoist MCP — *by abhiz123*
> Task management, projects & productivity tracking
> 
> 🔗 [GitHub](https://github.com/abhiz123/todoist-mcp-server) · 📇 TypeScript

```json
{
  "mcpServers": {
    "todoist": {
      "command": "npx",
      "args": ["-y", "@abhiz123/todoist-mcp-server"],
      "env": {
        "TODOIST_API_TOKEN": "your-todoist-token"
      }
    }
  }
}
```

---

#### 34. Obsidian MCP — *by MarkusPfworlds*
> Access Obsidian vault, notes, search & knowledge graph
> 
> 🔗 [GitHub](https://github.com/MarkusPfworlds/obsidian-mcp) · 📇 TypeScript

```json
{
  "mcpServers": {
    "obsidian": {
      "command": "npx",
      "args": ["-y", "obsidian-mcp"],
      "env": {
        "OBSIDIAN_VAULT_PATH": "/path/to/your/vault"
      }
    }
  }
}
```

---

#### 35. Airtable MCP — *by felores*
> Airtable bases, tables, records & field management
> 
> 🔗 [GitHub](https://github.com/felores/airtable-mcp) · 📇 TypeScript

```json
{
  "mcpServers": {
    "airtable": {
      "command": "npx",
      "args": ["-y", "airtable-mcp"],
      "env": {
        "AIRTABLE_API_KEY": "your-airtable-key"
      }
    }
  }
}
```

---

#### 36. Raycast MCP — *by Raycast*
> Productivity launcher, extensions & AI commands
> 
> 🔗 [GitHub](https://github.com/raycast/mcp-server-raycast) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "raycast": {
      "command": "npx",
      "args": ["-y", "@anthropic/raycast-mcp-server"]
    }
  }
}
```

---

### 💰 Finance & Payments (4 servers)

#### 37. Stripe MCP — *by Stripe, Inc.*
> Payment processing, subscriptions, invoices & customers
> 
> 🔗 [GitHub](https://github.com/stripe/agent-toolkit) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "stripe": {
      "command": "npx",
      "args": ["-y", "@stripe/agent-toolkit", "mcp"],
      "env": {
        "STRIPE_SECRET_KEY": "sk_your-stripe-key"
      }
    }
  }
}
```

---

#### 38. Dodo Payments MCP — *by Dodo Payments*
> Global payments, subscriptions, licenses & usage billing
> 
> 🔗 [npm](https://www.npmjs.com/package/@dodopayments/mcp-server) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "dodo-payments": {
      "command": "npx",
      "args": ["-y", "@dodopayments/mcp-server"],
      "env": {
        "DODO_PAYMENTS_API_KEY": "your-dodo-key"
      }
    }
  }
}
```

---

#### 39. Plaid MCP — *by ruchernchong*
> Banking connections, transactions & financial data
> 
> 🔗 [GitHub](https://github.com/ruchernchong/plaid-mcp-server) · 📇 TypeScript

```json
{
  "mcpServers": {
    "plaid": {
      "command": "npx",
      "args": ["-y", "plaid-mcp-server"],
      "env": {
        "PLAID_CLIENT_ID": "your-client-id",
        "PLAID_SECRET": "your-secret"
      }
    }
  }
}
```

---

#### 40. CoinGecko MCP — *by hisanibrahim*
> Cryptocurrency prices, market data & token info
> 
> 🔗 [GitHub](https://github.com/hisanibrahim/coingecko-mcp-server) · 📇 TypeScript

```json
{
  "mcpServers": {
    "coingecko": {
      "command": "npx",
      "args": ["-y", "coingecko-mcp-server"],
      "env": {
        "COINGECKO_API_KEY": "your-coingecko-key"
      }
    }
  }
}
```

---

### 📁 File Systems & Storage (4 servers)

#### 41. Filesystem MCP — *by Anthropic (Official)*
> Read/write local files with configurable access controls
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/allowed/directory"]
    }
  }
}
```

---

#### 42. AWS S3 MCP — *by Amazon Web Services*
> S3 bucket management, object operations & presigned URLs
> 
> 🔗 [GitHub](https://github.com/awslabs/mcp) · 🐍 Python · 🎖️ Official

```json
{
  "mcpServers": {
    "s3": {
      "command": "uvx",
      "args": ["awslabs.s3-mcp-server"],
      "env": {
        "AWS_ACCESS_KEY_ID": "your-key",
        "AWS_SECRET_ACCESS_KEY": "your-secret",
        "AWS_REGION": "us-east-1"
      }
    }
  }
}
```

---

#### 43. Memory MCP — *by Anthropic (Official)*
> Persistent knowledge graph for long-term AI memory
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "memory": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-memory"]
    }
  }
}
```

---

#### 44. Google Cloud Storage MCP — *by gcloudmcp*
> Google Cloud Storage bucket & object management
> 
> 🔗 [GitHub](https://github.com/nickarora/gcs-mcp-server) · 📇 TypeScript

```json
{
  "mcpServers": {
    "gcs": {
      "command": "npx",
      "args": ["-y", "gcs-mcp-server"],
      "env": {
        "GOOGLE_APPLICATION_CREDENTIALS": "/path/to/credentials.json"
      }
    }
  }
}
```

---

### 🧠 AI & ML (3 servers)

#### 45. Sequential Thinking MCP — *by Anthropic (Official)*
> Step-by-step reasoning engine for complex problem solving
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "sequentialthinking": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sequentialthinking"]
    }
  }
}
```

---

#### 46. Everart MCP — *by Anthropic (Official)*
> AI image generation & creative tools
> 
> 🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/everart) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "everart": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-everart"],
      "env": {
        "EVERART_API_KEY": "your-everart-key"
      }
    }
  }
}
```

---

#### 47. HuggingFace MCP — *by community*
> Access HuggingFace models, datasets & spaces
> 
> 🔗 [GitHub](https://github.com/mcpintegrations/huggingface-mcp) · 🐍 Python

```json
{
  "mcpServers": {
    "huggingface": {
      "command": "uvx",
      "args": ["huggingface-mcp"],
      "env": {
        "HF_TOKEN": "your-huggingface-token"
      }
    }
  }
}
```

---

### 💬 Communication (3 servers)

#### 48. Twilio MCP — *by Twilio*
> SMS, voice calls, WhatsApp & communication APIs
> 
> 🔗 [GitHub](https://github.com/twilio/mcp-server-twilio) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "twilio": {
      "command": "npx",
      "args": ["-y", "@twilio/mcp-server"],
      "env": {
        "TWILIO_ACCOUNT_SID": "your-account-sid",
        "TWILIO_AUTH_TOKEN": "your-auth-token"
      }
    }
  }
}
```

---

#### 49. Discord MCP — *by v-3*
> Discord bot, messages, channels & server management
> 
> 🔗 [GitHub](https://github.com/v-3/discord-mcp) · 📇 TypeScript

```json
{
  "mcpServers": {
    "discord": {
      "command": "npx",
      "args": ["-y", "discord-mcp"],
      "env": {
        "DISCORD_TOKEN": "your-discord-bot-token"
      }
    }
  }
}
```

---

#### 50. Email MCP — *by resend*
> Send emails via Resend API
> 
> 🔗 [GitHub](https://github.com/resend/mcp-send-email) · 📇 TypeScript · 🎖️ Official

```json
{
  "mcpServers": {
    "email": {
      "command": "npx",
      "args": ["-y", "@resend/mcp-send-email"],
      "env": {
        "RESEND_API_KEY": "re_your-resend-key"
      }
    }
  }
}
```

---

## 📊 Stats

| Metric | Count |
|---|---|
| **Total MCP Servers** | 50+ |
| **Categories** | 10 |
| **With Install Guides** | ✅ All 50 |
| **Official (🎖️)** | 28 |
| **Protocol** | [Model Context Protocol](https://modelcontextprotocol.io) |

---

## 🤝 How to Contribute

Know a great MCP server? Add it to the list!

### Quick Steps

1. ⭐ **Star this repo**
2. 🍴 **Fork** this repository
3. ✏️ **Add** your MCP server with install guide
4. 📤 **Submit a Pull Request**

👉 **Full guidelines:** [CONTRIBUTING.md](CONTRIBUTING.md)

### Entry Format
```markdown
#### Server Name — *by Company/Author*
> Short description
> 
> 🔗 [GitHub](link) · 📇 TypeScript · 🎖️ Official

\```json
{
  "mcpServers": {
    "server-name": {
      "command": "npx",
      "args": ["-y", "@package/name"],
      "env": {
        "API_KEY": "your-key"
      }
    }
  }
}
\```
```

### Requirements
- ✅ Must implement MCP (Model Context Protocol)
- ✅ Must have a public repository
- ✅ Must include install config snippet
- ✅ Must credit the original author/company
- ✅ Actively maintained (commits within 6 months)

---

## 🏷️ Legend

| Badge | Meaning |
|---|---|
| 🎖️ | Official implementation by the company |
| 📇 | TypeScript/JavaScript |
| 🐍 | Python |
| 🏎️ | Go |
| 🦀 | Rust |

---

## 🔗 Related Projects

| Project | Description |
|---|---|
| [modelcontextprotocol.io](https://modelcontextprotocol.io) | Official MCP specification by Anthropic |
| [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) | Official reference MCP servers |
| [claude-skills](https://github.com/skillsdirectory/claude-skills) | Agent Skills for Claude |
| [awesome-ai-skills](https://github.com/skillsdirectory/awesome-ai-skills) | Agent Skills for all AI tools |
| [agentskills.io](https://agentskills.io) | Agent Skills open standard |

---

## 📄 License

[CC0 1.0 Universal](LICENSE) — Free to use, modify, and share.

---

## ⚖️ Disclaimer

> **This is an independent, community-maintained project.**
>
> - This repository is **NOT** affiliated with, endorsed by, sponsored by, or associated with **any** of the companies, organizations, or products referenced herein, including but not limited to:
>   - **Anthropic** (Model Context Protocol, Claude)
>   - **MongoDB, ClickHouse, Turso, CockroachDB** (Databases)
>   - **Supabase, Neon, Redis** (Database platforms)
>   - **Stripe, Dodo Payments** (Payment providers)
>   - **GitHub / Microsoft, GitLab** (Developer platforms)
>   - **Docker, Cloudflare, Vercel, Netlify** (Infrastructure)
>   - **Google / Alphabet** (Drive, Maps, Cloud Storage)
>   - **Slack / Salesforce, Notion** (Productivity)
>   - **Sentry, Linear, Figma, Raycast** (Developer tools)
>   - **Brave, EXA, Tavily** (Search)
>   - **Twilio, Resend** (Communication)
>   - **Amazon / AWS** (Cloud services)
>   - Any other company, tool, service, or MCP server listed in this repository
> - All product names, trademarks, and registered trademarks are the property of their respective owners. Use of these names is solely for **informational and compatibility purposes** and is considered nominative fair use.
> - The **Model Context Protocol (MCP)** is an open standard. This repository curates MCP servers independently.
> - Listings are for **informational purposes only** and do not constitute endorsement.
> - Install configs are provided as **examples only**. Always refer to the official documentation of each MCP server for the latest setup instructions.
> - This repository makes **no warranties** regarding functionality, security, or reliability. **Use at your own risk.**
> - Users should **independently verify** the security of any MCP server before connecting it to their AI tools.

---

<p align="center">
  <strong>🌟 Found this useful? Give us a ⭐ Star!</strong>
  <br /><br />
  <a href="https://aiagentbase.app/skills">
    <img src="https://img.shields.io/badge/🚀_Deploy_MCP_Servers-AiAgentBase.app-FF6B35?style=for-the-badge" alt="AiAgentBase" />
  </a>
</p>
