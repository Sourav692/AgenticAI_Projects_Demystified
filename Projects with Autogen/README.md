# Projects with AutoGen

Hands-on projects built with [Microsoft AutoGen](https://github.com/microsoft/autogen), progressing from basic two-agent conversations to multi-agent GroupChat orchestration, tool use, RAG, and full-stack Streamlit deployments.

## Projects

| # | Project | What It Demonstrates |
|---|---------|----------------------|
| 0 | [Some Simple Agents](#0-some-simple-agents) | AssistantAgent, UserProxyAgent, code execution, GroupChat, multi-agent research teams |
| 1 | [Smart Content Generation](#1-smart-content-generation) | Two-agent create-then-critique collaboration |
| 2 | [Smart Health Assistant](#2-smart-health-assistant) | Sequential multi-agent pipeline with BMI tool, diet & workout planning |
| 3 | [Financial Portfolio Manager](#3-financial-portfolio-manager) | GroupChat with custom `state_transition` for conditional routing (StateFlow) |
| 4 | [Agentic RAG for eCommerce](#4-agentic-rag-for-ecommerce) | RAG with ChromaDB vector search for product and order retrieval |
| 5 | [Stock Market Analysis Agent](#5-stock-market-analysis-agent) | Full-stack Streamlit app with finance tools (yfinance, SMA, EMA, RSI) |

---

### 0. Some Simple Agents

Foundational notebooks covering core AutoGen concepts.

| Notebook | Focus |
|----------|-------|
| `1. Building Agents with AutoGen` | Introduction to AutoGen — LLM config, AssistantAgent, UserProxyAgent |
| `1. basic_agent` | Minimal agent setup and execution |
| `2. Building a Research Assistant with AutoGen` | Research assistant with web search |
| `2. coding_agent` | Code generation and execution agent |
| `3. research_team` | Multi-agent research team with 6 specialized roles: Admin, Engineer, Scientist, Planner, Executor, Critic |

**LLM Config:** Groq (`llama-3.3-70b-versatile`, `openai/gpt-oss-120b`) via `CONFIG_LIST.json`

**Dependencies:** `autogen-agentchat==0.2.38`, `groq`

---

### 1. Smart Content Generation

A two-agent collaboration where one agent generates content and another critiques and refines it through iterative feedback loops.

---

### 2. Smart Health Assistant

A sequential multi-agent pipeline that calculates BMI using a custom tool, then generates personalized diet and workout plans through specialized agents.

---

### 3. Financial Portfolio Manager

Demonstrates AutoGen's GroupChat with a custom `state_transition` function for conditional agent routing (StateFlow pattern), enabling structured financial portfolio analysis and management.

---

### 4. Agentic RAG for eCommerce

An agentic RAG system using ChromaDB for vector storage, enabling intelligent product search and order retrieval through natural language queries in an e-commerce context.

---

### 5. Stock Market Analysis Agent

A full-stack Streamlit application for AI-powered stock market analysis.

| File | Purpose |
|------|---------|
| `app.py` | Streamlit UI and entry point |
| `agents.py` | Agent definitions and roles |
| `agent_orchestrator.py` | Multi-agent orchestration logic |
| `agent_config.py` | Agent configuration |
| `app_config.py` | Application settings |
| `tools.py` | Finance tools (yfinance, SMA, EMA, RSI) |

**Run:**

```bash
cd "5. Stock Market Analysis Agent"
pip install -r requirements.txt
streamlit run app.py
```

**Dependencies:** `streamlit`, `openai`, `python-dotenv`, `yfinance`, `autogen`

---

## Technologies

| Category | Technologies |
|----------|-------------|
| **Agent Framework** | Microsoft AutoGen (0.2.x) |
| **LLM Providers** | OpenAI (GPT-4), Groq (Llama 3.3 70B) |
| **Vector Database** | ChromaDB |
| **Finance Data** | yfinance |
| **Web UI** | Streamlit |

## Prerequisites

- Python 3.9+
- API keys: OpenAI and/or Groq
- Create a `.env` file with your API keys

## Getting Started

```bash
# Install dependencies for simple agents
pip install -r "0. Some Simple Agents/requirements.txt"

# Install dependencies for Stock Market app
pip install -r "5. Stock Market Analysis Agent/requirements.txt"

# Run notebooks with Jupyter
jupyter notebook

# Run Stock Market Streamlit app
cd "5. Stock Market Analysis Agent"
streamlit run app.py
```
