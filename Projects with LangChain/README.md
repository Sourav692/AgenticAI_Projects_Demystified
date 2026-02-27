# Projects with LangChain

Hands-on projects built with [LangChain](https://github.com/langchain-ai/langchain), covering foundational LLM application patterns through agentic AI systems with tool calling, ReAct agents, RAG, SQL generation, and multi-user conversational memory.

## Projects

| # | Project | What It Demonstrates |
|---|---------|----------------------|
| 0 | [Some Simple Projects](#0-some-simple-projects-with-langchain) | Prompt templates, chains, streaming, conversational agents, structured output |
| 1 | [Agentic AI Research Assistant](#1-agentic-ai-research-assistant) | Tool-calling agent with research capabilities |
| 2 | [Multi-User Conversational Research Agents](#2-multi-user-conversational-research-agents) | Multi-user sessions with SQL-backed memory |
| 3 | [Text-to-SQL AI Systems](#3-text-to-sql-ai-systems) | Deterministic workflow vs. ReAct agent for natural language to SQL |
| 4 | [Financial Analyst Agent](#4-financial-analyst-agent) | ReAct agent with OpenBB financial data tools |
| 5 | [Intelligent Travel Assistant](#5-intelligent-travel-assistant) | Multi-tool travel planning agent |

---

### 0. Some Simple Projects with LangChain

Eleven examples covering LangChain fundamentals and common application patterns.

| Notebook / File | Focus |
|-----------------|-------|
| `Setup_Env` | Environment setup — LangChain, OpenAI installation and API key configuration |
| `1. Create a Review Analyst` | Prompt templates and chains for review analysis |
| `2. Create Research Paper Analyst` | Research paper analysis with structured prompts |
| `3. Create Social Media Marketing Analyst` | Social media marketing content generation |
| `4. IT Support Analyst` | IT support ticket analysis and resolution |
| `5. Building a Customer Support Workflow` | Multi-step customer support pipeline |
| `6. Building a Report Generator` | Automated report generation from data |
| `7. Building a Customer Review Analyst` | Customer review sentiment and insight extraction |
| `8. Build a Multi-user Conversational Product Recommendation Agent` | Product recommendations with per-user conversation memory |
| `9. Study Assistant for Quiz Question Generation` | Automated quiz question generation from study material |
| `10. chat_stream.py` | LLM response streaming implementation |
| `11. project_custom_chatgpt_with_langchain_from_scratch` | Building a custom ChatGPT clone from scratch |

---

### 1. Agentic AI Research Assistant

A tool-calling research assistant agent that can search the web, retrieve documents, and synthesize findings into structured research output.

---

### 2. Multi-User Conversational Research Agents

A multi-user conversational research agent with SQL-backed memory, enabling persistent conversation history across sessions and users.

---

### 3. Text-to-SQL AI Systems

Two approaches to natural language SQL generation, both using the same comic book database:

| Notebook | Approach |
|----------|----------|
| `1_Text2SQL_Deterministic_Workflow` | Deterministic chain — schema extraction, query generation, execution, and response formatting |
| `2_Text2SQL_ReAct_Agent` | ReAct agent — autonomous reasoning and tool use for dynamic SQL generation |

Includes `comicdb_create_script.sql` for database schema setup.

---

### 4. Financial Analyst Agent

A ReAct-based financial analyst agent powered by [OpenBB](https://openbb.co/) for real-time financial data access, market analysis, and investment insights.

---

### 5. Intelligent Travel Assistant

An intelligent travel planning agent that combines multiple tools — search, weather, maps, booking — to create comprehensive travel itineraries through natural language conversation.

---

## Technologies

| Category | Technologies |
|----------|-------------|
| **Agent Framework** | LangChain, LangGraph |
| **LLM Providers** | OpenAI, Groq, Databricks |
| **Vector Database** | ChromaDB |
| **Data Tools** | OpenBB, SQL databases |
| **Web Search** | Tavily, SerperDev |
| **Web UI** | Streamlit |

## Prerequisites

- Python 3.9+
- API keys: OpenAI and/or Groq
- Additional API keys depending on the project (Tavily, Serper, OpenBB)
- Create a `.env` file with your API keys

## Getting Started

```bash
# Install dependencies
pip install -r requirements.txt

# Run notebooks with Jupyter
jupyter notebook

# For Text-to-SQL projects, set up the database first
# using comicdb_create_script.sql
```

## Resources

- [LangChain in Action: Develop LLM-Powered Applications](https://www.udemy.com/course/langchain-in-action-develop-llm-powered-applications) (Udemy)
- [Introduction to LangChain for Agentic AI](https://courses.analyticsvidhya.com/courses/take/introduction-to-langchain-for-agentic-ai/) (Analytics Vidhya)
- [Building AI Agents with LangChain](https://courses.analyticsvidhya.com/courses/take/building-ai-agents-with-langchain/) (Analytics Vidhya)

## License

This project is licensed under the [MIT License](LICENSE).
