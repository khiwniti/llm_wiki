# BiteBase Ecosystem — Component Catalog

> Complete inventory of 33 repositories in the BiteBase ecosystem, classified by layer, category, and maturity.

---

## 📊 Summary

| Metric | Count |
|--------|-------|
| Total Repositories | 33 |
| Knowledge Graph Edges | 206 |
| Clusters | 8 |
| Technologies | 25 |
| Frontend Components | 11 |
| Full Stack Components | 2 |
| Backend Components | 1 |
| AI Services | 2 |
| Tooling | 5 |
| Unlisted/Config | 12 |

---

## 🏗️ Architecture Layers

### Full Stack (2)

| Repository | Description | Frameworks | Stack | Maturity |
|-----------|-------------|------------|-------|----------|
| **bitebase-v2** | Core platform v2 — restaurant discovery + AI copilot + backend | Next.js, React, Express, Tailwind CSS, OpenAI, LangChain, CopilotKit, Drizzle ORM, Recharts | TypeScript/JavaScript | active |
| **bitebase-ai-workspace** | AI workspace with Express backend + Next.js frontend | Next.js, React, Express, Tailwind CSS, Recharts, PostgreSQL, Redis | TypeScript/JavaScript | active |

### Frontend (11)

| Repository | Description | Frameworks | Stack | Maturity |
|-----------|-------------|------------|-------|----------|
| **bitebase-ai** | Core platform — restaurant discovery + Supabase | Next.js, React, Tailwind CSS, Prisma, Supabase, Mapbox, Zustand, PostgreSQL | TypeScript/JavaScript | active |
| **enhancement-bitebase-ai** | Enhanced AI platform with LangChain + OpenAI | Next.js, React, Tailwind CSS, Prisma, Supabase, OpenAI, LangChain, Mapbox, PostgreSQL | TypeScript/JavaScript | evolution |
| **bitebase-intelligence-v2** | Market intelligence dashboard v2 | Next.js, React, Tailwind CSS, Supabase, Radix UI | TypeScript/JavaScript | iteration |
| **beta-bitebase-app** | Intelligence dashboard (beta) | Next.js, React, Tailwind CSS, Radix UI, Leaflet, Mapbox, D3.js, Recharts, Zustand, TanStack | TypeScript/JavaScript | experimental |
| **beta-bitebase-app-r1** | Intelligence dashboard R1 | Next.js, React, Tailwind CSS, Radix UI, Mapbox, D3.js, Recharts, TanStack | TypeScript/JavaScript | experimental |
| **bitebase-agentics-ai** | Agentic AI frontend with CopilotKit patterns | Next.js, React, Tailwind CSS, Radix UI, Mapbox, Recharts, Zustand | TypeScript/JavaScript | active |
| **bitebase-agent-** | AI Restaurant Market Research dashboard | React, Vite | TypeScript/JavaScript | active |
| **bitebase-prototype.app** | Early prototype with Supabase + Leaflet | React, Tailwind CSS, Supabase, Radix UI, Leaflet, Recharts, Vite | TypeScript/JavaScript | experimental |
| **prototype.bitebase.app** | Full prototype with Prisma + Drizzle | Next.js, React, Tailwind CSS, Prisma, OpenAI, Radix UI, Recharts, Drizzle ORM, PostgreSQL | TypeScript/JavaScript | experimental |
| **llm_wiki** | Self-building personal knowledge base (Tauri desktop) | React, Tailwind CSS, shadcn/ui, Vite, Sigma.js, Zustand, Tauri | TypeScript/JavaScript + Rust | active |
| **beta-bitebase** | Beta with Turborepo monorepo | Next.js, Mapbox, Turborepo | TypeScript/JavaScript | experimental |

### Backend (1)

| Repository | Description | Frameworks | Stack | Maturity |
|-----------|-------------|------------|-------|----------|
| **bitebase-backend-express** | Standalone Express.js API for restaurant discovery | Express, OpenAI, Mapbox, PostgreSQL, Redis | TypeScript/JavaScript | active |

### AI Services (2)

| Repository | Description | Frameworks | Stack | Maturity |
|-----------|-------------|------------|-------|----------|
| **agentic-ai-agent.bitebase.app** | Python AI agent with LangChain + OpenAI | LangChain, OpenAI, Pandas | Python | active |
| **Bitebase-Agentic-AI-Infrastructure** | CopilotKit infrastructure for AI agents (fork) | CopilotKit | TypeScript/JavaScript | active |

### Tooling (5)

| Repository | Description | Frameworks | Stack | Maturity |
|-----------|-------------|------------|-------|----------|
| **bitebase-geospatial-saas** | Geospatial SaaS tooling with Turborepo | Mapbox, Turborepo | TypeScript/JavaScript | active |
| **bitebase-intelligence** | Intelligence tooling with Turborepo | Mapbox, Turborepo | TypeScript/JavaScript | active |
| **enhancement-bitebase-intelligence** | Intelligence enhancement tooling | — | JavaScript | evolution |
| **bitebase-ui** | UI component library (fork of StudioCMS) | — | TypeScript/JavaScript | active |
| **mcp-server-bitebase-app** | MCP (Model Context Protocol) server | — | TypeScript/JavaScript | active |

### Config / Design / Other (12)

| Repository | Category | Notes |
|-----------|----------|-------|
| **bitebase-ai-agents** | ai-agent | Agent configuration |
| **bitebase-coagents** | coagents | CoAgents setup |
| **BiteBase-Intelligence-R1** | intelligence | R1 iteration |
| **bitebase-orchestration-design** | orchestration | Workflow design docs |
| **bitebase-workspace.coder** | workspace | Coder workspace config |
| **bitebase-beta-app-r1** | prototype | Beta R1 config |
| **_authenticationAPI.BiteBase.app** | authentication | Auth API service |
| **agentic-workflows.bitebase.app** | workflow | Workflow definitions |
| **prelunch-bitebase-app** | prototype | Pre-launch config |
| **prelunch.bitebase.app** | prototype | Pre-launch config |
| **bolt-new.bitebase.app** | core | Bolt.new generated |
| **style-guide.bitebase.github.io** | ui-library | CSS style guide |

---

## 🔗 Relationship Types

| Type | Description | Color |
|------|-------------|-------|
| `serves` | Backend serves frontend | 🟡 Amber |
| `evolved_to` | Repository evolved/iterates to another | 🟢 Green |
| `enhances` | Enhancement layer on top of existing repo | 🔵 Cyan |
| `infra_for` | Infrastructure component for agents | 🟣 Indigo |
| `merged_into` | Changes merged into target repo | 🩷 Pink |
| `extends` | MCP protocol extension | 🩵 Teal |
| `auth_for` | Authentication service dependency | 🟠 Orange |
| `consumed_by` | UI library consumed by app | 🩷 Pink |
| `geo_layer_for` | Geospatial data layer | 🟡 Amber |
| `shared_framework` | Both repos share a framework | 🔵 Blue |
| `same_category` | Same functional category | 🟣 Purple |

---

## 🧩 Reusable Components for Future Projects

### 🔮 High Reuse Potential

| Component | Source | Reuse For |
|-----------|--------|-----------|
| **Mapbox Restaurant Discovery** | bitebase-ai, bitebase-v2 | Any geo-aware SaaS |
| **CopilotKit AI Chat** | Bitebase-Agentic-AI-Infrastructure | Any app needing AI copilot |
| **Intelligence Dashboard** | bitebase-intelligence-v2 | Analytics/market research apps |
| **Auth API** | _authenticationAPI.BiteBase.app | Any BiteBase microservice |
| **MCP Server** | mcp-server-bitebase-app | LLM integration layer |
| **UI Component Library** | bitebase-ui | Shared design system |
| **Knowledge Graph Engine** | llm_wiki | Any knowledge management app |
| **Express Backend API** | bitebase-backend-express | Restaurant/hospitality backends |
| **Geospatial SaaS Kit** | bitebase-geospatial-saas | Location-based applications |

### 🔄 Cross-Project Patterns

| Pattern | Repos Using It | Description |
|---------|---------------|-------------|
| **Next.js + Tailwind + Radix** | 10+ repos | Standard frontend stack |
| **Supabase Auth + DB** | bitebase-ai, enhancement-bitebase-ai, bitebase-intelligence-v2, bitebase-prototype.app | Backend-as-a-service |
| **Prisma + PostgreSQL** | bitebase-ai, enhancement-bitebase-ai, prototype.bitebase.app | Type-safe ORM |
| **Drizzle ORM + PostgreSQL** | bitebase-v2, prototype.bitebase.app | Lightweight ORM |
| **Mapbox + D3.js** | bitebase-ai, beta-bitebase-app, bitebase-geospatial-saas | Geospatial visualization |
| **OpenAI + LangChain** | bitebase-v2, enhancement-bitebase-ai, agentic-ai-agent.bitebase.app | LLM integration |
| **CopilotKit** | Bitebase-Agentic-AI-Infrastructure, bitebase-v2 | AI copilot UI |
| **Express + Redis** | bitebase-backend-express, bitebase-ai-workspace | Backend + caching |
| **Tauri + Rust** | llm_wiki | Cross-platform desktop |
| **Sigma.js + Graphology** | llm_wiki | Graph visualization |

---

## 📈 Evolution Timeline

```
prelunch-bitebase-app ──► beta-bitebase-app ──► bitebase-ai ──► bitebase-v2
                                │                               ▲
                                ▼                               │
                         beta-bitebase-app-r1     enhancement-bitebase-ai
                         
bitebase-intelligence ──► BiteBase-Intelligence-R1 ──► bitebase-intelligence-v2
                                                            ▲
                                        enhancement-bitebase-intelligence

bitebase-prototype.app ──► prototype.bitebase.app ──► bitebase-v2
bolt-new.bitebase.app ───┘

Bitebase-Agentic-AI-Infrastructure ──► bitebase-agentics-ai
                                       bitebase-coagents
                                       
bitebase-ai-agents ──► agentic-ai-agent.bitebase.app (Python)
                    ──► agentic-workflows.bitebase.app
```