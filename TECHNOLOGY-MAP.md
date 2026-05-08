# BiteBase Ecosystem — Technology Map

> Which technologies are used across the BiteBase ecosystem, and which repos share them.

---

## 🛠️ Technology Adoption Matrix

| Technology | Repos Using | Category |
|-----------|-------------|----------|
| **Next.js** | bitebase-ai, bitebase-v2, enhancement-bitebase-ai, bitebase-intelligence-v2, beta-bitebase-app, beta-bitebase-app-r1, bitebase-agentics-ai, bitebase-ai-workspace, prototype.bitebase.app, beta-bitebase | Frontend Framework |
| **React** | bitebase-ai, bitebase-v2, enhancement-bitebase-ai, bitebase-intelligence-v2, beta-bitebase-app, beta-bitebase-app-r1, bitebase-agentics-ai, bitebase-ai-workspace, bitebase-agent-, bitebase-prototype.app, prototype.bitebase.app, llm_wiki | UI Library |
| **Tailwind CSS** | bitebase-ai, bitebase-v2, enhancement-bitebase-ai, bitebase-intelligence-v2, beta-bitebase-app, beta-bitebase-app-r1, bitebase-agentics-ai, bitebase-ai-workspace, bitebase-prototype.app, prototype.bitebase.app, llm_wiki | Styling |
| **Radix UI** | bitebase-ai, bitebase-v2, enhancement-bitebase-ai, bitebase-intelligence-v2, beta-bitebase-app, beta-bitebase-app-r1, bitebase-agentics-ai | Component Library |
| **Mapbox** | bitebase-ai, bitebase-v2, enhancement-bitebase-ai, bitebase-backend-express, beta-bitebase-app, beta-bitebase-app-r1, bitebase-agentics-ai, bitebase-geospatial-saas, bitebase-intelligence | Maps/Geo |
| **Express** | bitebase-v2, bitebase-backend-express, bitebase-ai-workspace | Backend Framework |
| **PostgreSQL** | bitebase-ai, bitebase-backend-express, enhancement-bitebase-ai, bitebase-ai-workspace, prototype.bitebase.app | Database |
| **OpenAI** | bitebase-v2, enhancement-bitebase-ai, bitebase-backend-express, prototype.bitebase.app, agentic-ai-agent.bitebase.app | AI/LLM |
| **LangChain** | bitebase-v2, enhancement-bitebase-ai, agentic-ai-agent.bitebase.app | AI Framework |
| **CopilotKit** | Bitebase-Agentic-AI-Infrastructure, bitebase-v2 | AI Copilot UI |
| **Supabase** | bitebase-ai, enhancement-bitebase-ai, bitebase-intelligence-v2, bitebase-prototype.app | BaaS |
| **Prisma** | bitebase-ai, enhancement-bitebase-ai, prototype.bitebase.app | ORM |
| **Drizzle ORM** | bitebase-v2, prototype.bitebase.app | ORM |
| **Redis** | bitebase-backend-express, bitebase-ai-workspace | Caching |
| **Recharts** | bitebase-v2, beta-bitebase-app, beta-bitebase-app-r1, bitebase-agentics-ai, bitebase-ai-workspace, bitebase-prototype.app, prototype.bitebase.app | Charts |
| **D3.js** | beta-bitebase-app, beta-bitebase-app-r1, llm_wiki | Data Viz |
| **Zustand** | bitebase-ai, beta-bitebase-app, bitebase-agentics-ai, llm_wiki | State Mgmt |
| **TanStack** | bitebase-v2, beta-bitebase-app, beta-bitebase-app-r1 | Data Query |
| **Vite** | bitebase-agent-, bitebase-prototype.app, llm_wiki | Build Tool |
| **Turborepo** | beta-bitebase, bitebase-geospatial-saas, bitebase-intelligence | Monorepo |
| **Leaflet** | beta-bitebase-app, bitebase-prototype.app | Maps |
| **Tauri** | llm_wiki | Desktop Framework |
| **Sigma.js** | llm_wiki | Graph Viz |
| **shadcn/ui** | llm_wiki | Component Library |
| **FastAPI** | agentic-ai-agent.bitebase.app | Python Backend |

---

## 🔗 Shared Dependency Graph

Technologies that commonly appear together in BiteBase repos:

```
Next.js ──── React ──── Tailwind CSS ──── Radix UI
   │            │            │               │
   │            │            └── shadcn/ui (llm_wiki)
   │            │            │
   │            ├── Zustand (state)
   │            ├── Recharts (charts)
   │            └── TanStack (data)
   │
   ├── Mapbox (maps) ──── Leaflet (alt maps)
   ├── Prisma ──── PostgreSQL
   ├── Drizzle ORM ──── PostgreSQL  
   ├── Supabase (auth + db)
   └── Vite (build, non-Next)

Express ──── Redis ──── PostgreSQL
   │
   └── OpenAI ──── LangChain

CopilotKit ──── bitebase-v2 ──── bitebase-agentics-ai

Tauri ──── Rust ──── LanceDB ──── Sigma.js (llm_wiki)

FastAPI ──── LangChain ──── OpenAI ──── Pandas (Python agent)
```

---

## 📊 Stack Combinations

| Stack Pattern | Repos | Count |
|--------------|-------|-------|
| Next.js + React + Tailwind + Radix + Mapbox | bitebase-ai, bitebase-v2, enhancement-bitebase-ai, beta-bitebase-app, bitebase-agentics-ai | 5 |
| Next.js + React + Tailwind + Supabase | bitebase-ai, enhancement-bitebase-ai, bitebase-intelligence-v2, bitebase-prototype.app | 4 |
| Express + PostgreSQL + Redis | bitebase-backend-express, bitebase-ai-workspace | 2 |
| OpenAI + LangChain | bitebase-v2, enhancement-bitebase-ai, agentic-ai-agent.bitebase.app | 3 |
| Tauri + Rust + React | llm_wiki | 1 |
| Python + LangChain + OpenAI | agentic-ai-agent.bitebase.app | 1 |

---

## 🧭 Recommended Stack for New Full Stack Projects

Based on the most proven combinations across the ecosystem:

### Primary (Battle-Tested)
```
Frontend:  Next.js 14 + React 19 + Tailwind CSS + Radix UI + shadcn/ui
State:     Zustand
Charts:    Recharts
Maps:      Mapbox
ORM:       Drizzle ORM
Database:  PostgreSQL
Auth:      Supabase Auth
Backend:   Express.js (standalone) or Next.js API routes
Cache:     Redis
AI:        OpenAI + LangChain + CopilotKit
```

### Desktop Application
```
Shell:     Tauri v2 (Rust)
Frontend:  React + Vite + Tailwind CSS + shadcn/ui
State:     Zustand
Graph:     Sigma.js + Graphology
Vector DB: LanceDB (embedded, Rust)
Search:    Tokenized + Vector (LanceDB) + Graph Relevance
```

### AI Agent Service
```
Runtime:   Python 3.11+
Framework: LangChain + OpenAI
Server:    FastAPI
Data:      Pandas
MCP:       mcp-server-bitebase-app for LLM tool integration
```