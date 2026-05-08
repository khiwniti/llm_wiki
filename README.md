# 🧠 BiteBase Ecosystem — Knowledge Graph

> A comprehensive knowledge graph of the BiteBase full stack development ecosystem — 33 repositories, 8 clusters, 25 technologies, mapped and interconnected.

![Knowledge Graph](https://img.shields.io/badge/Nodes-33-blue) ![Edges](https://img.shields.io/badge/Edges-206-green) ![Clusters](https://img.shields.io/badge/Clusters-8-purple) ![Technologies](https://img.shields.io/badge/Tech-25-orange)

---

## 🗺️ What Is This?

This repository is a **knowledge graph of the entire BiteBase ecosystem** — all 33 related repositories from [github.com/khiwniti](https://github.com/khiwniti), analyzed, classified, and interconnected. It serves as:

1. **🗺️ Navigation Map** — Understand which repos depend on each other and why
2. **🧩 Reuse Guide** — Know which components can be combined in future projects
3. **📊 Architecture Reference** — See the full stack architecture at a glance
4. **🔮 Evolution Timeline** — Track how prototypes evolved into production systems

---

## 📂 Repository Structure

```
bitebase-ecosystem/
├── README.md                    ← You are here
├── COMPONENT-CATALOG.md         ← Full inventory of all 33 repos
├── TECHNOLOGY-MAP.md             ← Technology adoption & shared deps
├── knowledge-graph.html          ← Interactive D3.js visualization
├── knowledge-graph.json          ← Full graph data (33 nodes, 206 edges)
├── knowledge-graph-compact.json  ← Filtered graph (weight ≥ 3)
├── analysis.json                 ← Raw analysis data per repo
├── sources/                      ← Cloned source repos (33)
│   ├── bitebase-ai/
│   ├── bitebase-v2/
│   ├── bitebase-backend-express/
│   ├── llm_wiki/
│   └── ... (29 more)
└── .gitignore
```

---

## 🖥️ Interactive Visualization

Open `knowledge-graph.html` in any browser for the full interactive graph:

- **Zoom/Pan** — Scroll to zoom, drag to pan
- **Click nodes** — See repo details + highlight connections
- **Filter** — By category (ai-agent, intelligence, core...) or layer (frontend, backend, fullstack)
- **Search** — Type repo names in the search box
- **Legend** — Click cluster names to highlight groups
- **Drag nodes** — Reposition nodes in the force layout

### Node Shapes by Layer

| Shape | Layer | Examples |
|-------|-------|---------|
| ⬡ Hexagon | Full Stack | bitebase-v2, bitebase-ai-workspace |
| ● Circle | Frontend | bitebase-ai, bitebase-intelligence-v2 |
| ■ Square | Backend | bitebase-backend-express |
| ◆ Diamond | AI Service | agentic-ai-agent.bitebase.app |
| ▲ Triangle | Infrastructure | bitebase-orchestration-design |
| ★ Star | Tooling | bitebase-geospatial-saas, mcp-server-bitebase-app |

### Node Colors by Category

| Color | Category |
|-------|----------|
| 🔵 Blue | Core Platform |
| 🟣 Purple | Intelligence |
| 🟢 Green | AI Agents |
| 🟡 Amber | Geospatial |
| 🔴 Red | Prototypes |
| 🩷 Pink | UI & Design |
| 🟣 Indigo | Infrastructure |
| 🩵 Teal | Knowledge Base |

---

## 🏗️ Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                     BITEBASE ECOSYSTEM                          │
├──────────────┬──────────────┬───────────────┬──────────────────┤
│   FRONTEND   │   BACKEND    │   AI/AGENTS   │  INFRASTRUCTURE  │
├──────────────┼──────────────┼───────────────┼──────────────────┤
│ bitebase-ai  │ backend-     │ agent-        │ mcp-server       │
│ bitebase-v2  │ express      │ agentics-ai   │ orchestration    │
│ enhancement  │ auth API     │ ai-agents     │ workspace       │
│ intelligence │              │ coagents      │ style-guide      │
│ -v2          │              │ agentic-      │ bitebase-ui      │
│ beta-app     │              │ workflows     │                  │
│ agent-       │              │ infra         │                  │
├──────────────┼──────────────┼───────────────┼──────────────────┤
│   PROTOTYPES │   GEO        │  KNOWLEDGE    │  CONFIG          │
├──────────────┼──────────────┼───────────────┼──────────────────┤
│ prelunch-*   │ geospatial   │ llm_wiki      │ beta-app-r1     │
│ prototype*   │ saas         │ (Tauri+Rust)  │ Intelligence-R1 │
│ bolt-new     │              │               │ coder workspace │
│ beta-*       │              │               │                  │
└──────────────┴──────────────┴───────────────┴──────────────────┘
```

---

## 🧬 8 Clusters

### 1. Core Platform (🔵 Blue)
The main BiteBase product — restaurant discovery, AI copilot, backend API, authentication.

| Repo | Role | Key Tech |
|------|------|----------|
| `bitebase-ai` | Primary frontend | Next.js, React, Supabase, Mapbox |
| `bitebase-v2` | Next-gen full stack | Next.js, Express, LangChain, CopilotKit |
| `enhancement-bitebase-ai` | AI enhancement layer | OpenAI, LangChain, Prisma |
| `bitebase-backend-express` | Standalone backend | Express, PostgreSQL, Redis, OpenAI |
| `_authenticationAPI.BiteBase.app` | Auth microservice | — |

### 2. Intelligence (🟣 Purple)
Market intelligence dashboards, analytics, and business insights.

| Repo | Role | Key Tech |
|------|------|----------|
| `bitebase-intelligence` | v1 tooling | Mapbox, Turborepo |
| `bitebase-intelligence-v2` | v2 dashboard | Next.js, Supabase, Radix UI |
| `BiteBase-Intelligence-R1` | R1 iteration | — |
| `enhancement-bitebase-intelligence` | Enhancement | JavaScript |
| `beta-bitebase-app` | Beta dashboard | Next.js, Mapbox, D3.js, Recharts |
| `beta-bitebase-app-r1` | R1 variant | Next.js, Mapbox, D3.js |
| `bitebase-beta-app-r1` | R1 config | — |

### 3. AI Agents (🟢 Green)
Autonomous AI agents, CopilotKit infrastructure, and agentic workflows.

| Repo | Role | Key Tech |
|------|------|----------|
| `bitebase-agent-` | Agent dashboard UI | React, Vite |
| `bitebase-ai-agents` | Agent configurations | — |
| `Bitebase-Agentic-AI-Infrastructure` | CopilotKit infra (fork) | CopilotKit |
| `bitebase-coagents` | CoAgents setup | — |
| `agentic-ai-agent.bitebase.app` | Python agent service | LangChain, OpenAI, FastAPI |
| `agentic-workflows.bitebase.app` | Workflow definitions | — |
| `bitebase-agentics-ai` | Agentic AI frontend | Next.js, React, Mapbox, Zustand |

### 4. Geospatial (🟡 Amber)
Map-based restaurant discovery and geospatial analytics.

| Repo | Role | Key Tech |
|------|------|----------|
| `bitebase-geospatial-saas` | Geo SaaS tooling | Mapbox, Turborepo |

### 5. Prototypes & Iterations (🔴 Red)
Early versions, pre-launch builds, and experimental iterations.

| Repo | Role | Key Tech |
|------|------|----------|
| `prelunch-bitebase-app` | Pre-launch | — |
| `prelunch.bitebase.app` | Pre-launch | — |
| `bitebase-prototype.app` | Early prototype | React, Supabase, Leaflet |
| `prototype.bitebase.app` | Full prototype | Next.js, Prisma, Drizzle, OpenAI |
| `beta-bitebase` | Beta monorepo | Next.js, Turborepo |
| `bolt-new.bitebase.app` | Bolt.new generated | — |

### 6. UI & Design (🩷 Pink)
Shared component library and design system.

| Repo | Role | Key Tech |
|------|------|----------|
| `bitebase-ui` | UI components (fork) | TypeScript |
| `style-guide.bitebase.github.io` | CSS style guide | CSS |

### 7. Infrastructure (🟣 Indigo)
Orchestration, workspace management, MCP server, and dev tooling.

| Repo | Role | Key Tech |
|------|------|----------|
| `bitebase-orchestration-design` | Workflow design | — |
| `bitebase-workspace.coder` | Coder config | — |
| `bitebase-ai-workspace` | AI workspace (full stack) | Next.js, Express, PostgreSQL, Redis |
| `mcp-server-bitebase-app` | MCP protocol server | TypeScript |

### 8. Knowledge Base (🩵 Teal)
Self-building personal knowledge base with graph visualization.

| Repo | Role | Key Tech |
|------|------|----------|
| `llm_wiki` | Desktop knowledge app | Tauri v2, React, Sigma.js, LanceDB, Rust |

---

## 🔗 Key Relationships

### Backend → Frontend
```
bitebase-backend-express ──serves──► bitebase-ai
bitebase-backend-express ──serves──► bitebase-v2
bitebase-backend-express ──serves──► enhancement-bitebase-ai
bitebase-backend-express ──serves──► bitebase-agentics-ai
```

### Evolution Chains
```
prelunch-bitebase-app ──► beta-bitebase-app ──► bitebase-ai ──► bitebase-v2
bitebase-intelligence ──► bitebase-intelligence-v2
bitebase-prototype.app ──► prototype.bitebase.app ──► bitebase-v2
```

### AI Infrastructure
```
Bitebase-Agentic-AI-Infrastructure ──infra_for──► bitebase-agentics-ai
Bitebase-Agentic-AI-Infrastructure ──infra_for──► bitebase-coagents
bitebase-ai-agents ──deploys_as──► agentic-ai-agent.bitebase.app (Python)
```

### MCP Integration
```
mcp-server-bitebase-app ──extends──► bitebase-v2
mcp-server-bitebase-app ──extends──► enhancement-bitebase-ai
```

### Auth Dependency
```
_authenticationAPI.BiteBase.app ──auth_for──► bitebase-backend-express
_authenticationAPI.BiteBase.app ──auth_for──► bitebase-ai
```

### Knowledge Integration
```
llm_wiki ──knowledge_for──► bitebase-ai
llm_wiki ──knowledge_for──► bitebase-v2
```

---

## 🧩 Reuse Guide: Combining Components

### 🍽️ Restaurant Discovery Platform
```
bitebase-v2 (frontend+backend) + bitebase-backend-express (API)
+ bitebase-geospatial-saas (maps) + _authenticationAPI.BiteBase.app (auth)
+ mcp-server-bitebase-app (LLM tools)
```

### 🤖 AI Copilot Application
```
Bitebase-Agentic-AI-Infrastructure (CopilotKit) + bitebase-agentics-ai (UI)
+ agentic-ai-agent.bitebase.app (Python agent) + bitebase-coagents
```

### 📊 Market Intelligence Dashboard
```
bitebase-intelligence-v2 (dashboard) + bitebase-backend-express (data API)
+ enhancement-bitebase-intelligence (enhancements)
```

### 📝 Knowledge Management System
```
llm_wiki (Tauri desktop) + mcp-server-bitebase-app (MCP integration)
+ bitebase-ai (web knowledge layer)
```

### 🗺️ Geospatial SaaS
```
bitebase-geospatial-saas (tooling) + bitebase-ai (Mapbox integration)
+ bitebase-backend-express (geo API)
```

---

## 📊 Tech Stack Summary

| Layer | Primary | Alternative |
|-------|---------|-------------|
| Frontend | Next.js 14+ React 19 | React + Vite |
| Styling | Tailwind CSS + Radix UI | shadcn/ui |
| State | Zustand | TanStack Query |
| Maps | Mapbox | Leaflet |
| Charts | Recharts | D3.js |
| Backend | Express.js | Next.js API Routes |
| Database | PostgreSQL | Supabase |
| ORM | Drizzle ORM | Prisma |
| Cache | Redis | — |
| Auth | Supabase Auth | Custom Auth API |
| AI/LLM | OpenAI + LangChain | — |
| Copilot | CopilotKit | — |
| Desktop | Tauri v2 + Rust | — |
| Vector DB | LanceDB (embedded) | — |
| Graph Viz | Sigma.js + Graphology | D3.js |
| Search | Tokenized + Vector + Graph | — |
| Python AI | FastAPI + LangChain | — |
| Monorepo | Turborepo | — |
| Protocol | MCP (Model Context Protocol) | — |

---

## 🚀 Getting Started

### Browse the Knowledge Graph
```bash
# Open the interactive visualization
open knowledge-graph.html
# Or serve it locally
npx serve .
```

### Explore Source Code
```bash
# All 33 repos are in sources/
ls sources/

# Example: examine the core platform
cat sources/bitebase-v2/package.json
cat sources/bitebase-backend-express/package.json
```

### Use the Graph Data
```javascript
// Load the knowledge graph data
const graph = require('./knowledge-graph.json');

// Get all repos in a cluster
const coreRepos = graph.clusters["Core Platform"].repos;

// Get all edges for a repo
const edges = graph.edges.filter(e => e.source === "bitebase-v2" || e.target === "bitebase-v2");

// Get technology adoption
const nextjsRepos = graph.technology_map["Next.js"];
```

---

## 📜 License

This knowledge graph repository is provided for reference and navigation purposes.
Individual source repositories retain their original licenses (see each repo's LICENSE file).

---

## 🙏 Credits

- **Andrej Karpathy** — LLM Wiki pattern that inspired the knowledge graph approach
- **khiwniti** — All 33 BiteBase ecosystem repositories
- **D3.js** — Force-directed graph visualization