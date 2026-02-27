# Projects with LangGraph

Hands-on projects built with [LangGraph](https://github.com/langchain-ai/langgraph), organized by difficulty level — from basic tool-use agents to production-grade multi-agent systems with planning, reflection, and orchestration.

## Projects

### 01-Beginner

Entry-level projects for getting started with LangGraph agents.

| Project | Description | Key Concepts |
|---------|-------------|--------------|
| **Financial_Analyst_Tool_Use_Agent** | Build a financial analyst AI agent that uses custom tools | Tool-use, Function calling, Basic agent workflow |

### 02-Intermediate

Projects combining multiple concepts with more complex patterns.

| Project | Description | Key Concepts |
|---------|-------------|--------------|
| **Multi_User_Conversational_Financial_Agent** | Multi-user conversational agent with persistent memory | Memory, Threads, Multi-user sessions |
| **Customer_Support_Router_RAG** | Intelligent router with RAG for customer support | Router pattern, RAG, Sentiment analysis |
| **Reflective_Code_Generation_Agent** | Self-correcting code generation agent | Reflection pattern, Code execution, Iterative refinement |

The Customer Support Router project includes a Databricks-specific variant (`Customer_Support_Router_Agentic_RAG_Databricks.ipynb`) with Databricks-hosted models and a `router_agent_documents.json` knowledge base.

### 03-Advanced

Complex projects featuring advanced patterns and multi-agent architectures.

| Project | Description | Key Concepts |
|---------|-------------|--------------|
| **Planning_Agent_Deep_Research** | Deep research agent with structured report generation | Planning pattern, Parallel execution, Report synthesis |
| **Reflective_Dynamic_Planning_Agent** | Dynamic planning with reflection for complex queries | Dynamic replanning, Reflection, Multi-step execution |
| **Supervisor_Multi_Agent_Financial_Research** | Supervisor architecture for financial research | Supervisor pattern, Sub-agents, Task delegation |
| **Multi_Agent_Research_Summarization** | Research and summarization multi-agent system | Router, Web research, RAG, Summarization agents |

The Multi-Agent Research Summarization project includes supporting modules: `restaurant_knowledge_base.py` (RAG data) and `langgraph_research_agent_single.py` (standalone agent).

### 04-Full-Stack-Projects

Complete end-to-end projects with multiple modules.

| Project | Description | Key Concepts |
|---------|-------------|--------------|
| **Hotel_Reservations_Multi_Agent_System** | Full hotel reservation system with multiple specialized agents | Multi-agent orchestration, Error handling, Multi-language support |
| **Software_Engineering_Multi_Agent_System** | Developer vs Tester agents for software engineering workflows | Multi-actor systems, Agent collaboration |

#### Hotel Reservations System — Modules

| Module | Notebooks | Topics |
|--------|-----------|--------|
| **Module 2: Core Agents** | 6 notebooks | Environment setup, Booking Agent, Availability Agent, Customer Service Agent, Edge cases, Testing |
| **Module 3: Advanced Features** | 6 notebooks | Agent orchestration, Agent-to-agent communication, Multi-language support, Sentiment analysis, Error handling, Web search integration |

---

## LangGraph Patterns Covered

| Pattern | Projects |
|---------|----------|
| Tool-use agents | 01 (Financial Analyst) |
| Memory & threads | 02 (Multi-User Financial) |
| Router pattern | 02 (Customer Support), 03 (Research Summarization) |
| RAG integration | 02 (Customer Support), 03 (Research Summarization) |
| Reflection / self-correction | 02 (Code Generation), 03 (Dynamic Planning) |
| Planning pattern | 03 (Deep Research, Dynamic Planning) |
| Supervisor multi-agent | 03 (Financial Research) |
| Parallel execution | 03 (Deep Research) |
| Multi-agent orchestration | 04 (Hotel Reservations, Software Engineering) |
| Human-in-the-loop | 04 (Hotel Reservations) |

## Recommended Learning Path

1. Start with **01-Beginner** to understand tool-use basics
2. Progress through **02-Intermediate** to learn routing, memory, and reflection
3. Tackle **03-Advanced** for complex planning and multi-agent systems
4. Explore **04-Full-Stack-Projects** for complete production-ready implementations

## Technologies

| Category | Technologies |
|----------|-------------|
| **Agent Framework** | LangGraph, LangChain |
| **LLM Providers** | OpenAI, Groq, Databricks |
| **Vector Database** | ChromaDB |
| **Web Search** | Tavily |
| **Deployment** | Databricks |

## Prerequisites

- Python 3.9+
- LangChain and LangGraph packages
- OpenAI API key (or alternative LLM provider)
- Tavily API key (for web search projects)

See the root `requirements.txt` for all dependencies.

## Resources

- [Building Advanced AI Agents with LangGraph](https://courses.analyticsvidhya.com/courses/take/building-advanced-ai-agents-with-langgraph/) (Analytics Vidhya)
- [LangGraph AI Repository](https://github.com/piyushagni5/langgraph-ai) (GitHub)
