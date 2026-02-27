# Agentic AI Projects Demystified

A curated collection of hands-on projects exploring the major agentic AI frameworks — **AutoGen**, **CrewAI**, **LangChain**, and **LangGraph**. Each folder contains progressively complex examples, from single-agent basics to production-grade multi-agent systems with tool use, RAG, conditional routing, flows, and full-stack deployments.

## Repository Structure

```
AgenticAI_Projects_Demystified/
├── Projects with Autogen/       # Microsoft AutoGen — GroupChat, tool use, RAG, Streamlit apps
├── Projects with CrewAI/        # CrewAI — crews, flows, custom tools, memory, deployment
├── Projects with LangChain/     # LangChain-based agent projects
├── Projects with LangGraph/     # LangGraph-based agent projects
├── Full Stack Projects/         # End-to-end full-stack agentic applications
└── LICENSE                      # Apache 2.0
```

---

## Projects with AutoGen

Six projects built with [Microsoft AutoGen](https://github.com/microsoft/autogen), covering two-agent chat, GroupChat orchestration, tool use, RAG, conditional routing, and Streamlit deployments.

| # | Project | What It Demonstrates |
|---|---------|----------------------|
| 0 | **Some Simple Agents** | AssistantAgent, UserProxyAgent, code execution, GroupChat, multi-agent research teams |
| 1 | **Smart Content Generation** | Two-agent create-then-critique collaboration |
| 2 | **Smart Health Assistant** | Sequential multi-agent pipeline with BMI tool, diet & workout planning |
| 3 | **Financial Portfolio Manager** | GroupChat with custom `state_transition` for conditional routing (StateFlow) |
| 4 | **Agentic RAG for eCommerce** | RAG with ChromaDB vector search for product and order retrieval |
| 5 | **Stock Market Analysis Agent** | Full-stack Streamlit app with finance tools (yfinance, SMA, EMA, RSI) |

**Technologies:** AutoGen (0.2.x–0.10.x), OpenAI, Groq, ChromaDB, yfinance, Streamlit

See [`Projects with Autogen/README.md`](Projects%20with%20Autogen/README.md) for detailed descriptions.

---

## Projects with CrewAI

Ten project folders built with [CrewAI](https://github.com/crewAIInc/crewAI), progressing from single-crew patterns to advanced flows, conditional tasks, memory integration, custom tools, and Databricks deployment.

| # | Project | What It Demonstrates |
|---|---------|----------------------|
| 01 | **Some Simple AI Agents** | Eight examples covering Flows, DALL-E image generation, Mem0 memory, CodeInterpreterTool, ConditionalTask, custom tools, async crews, hierarchical processes |
| 02 | **Personalized Education Assistant** | Learning material curation with Pydantic structured output |
| 03 | **Multi-Agent Mock Interviewer** | Interview prep system with Streamlit UI, Whisper STT, Databricks Apps deployment |
| 04 | **Social Media Agent** | Platform-specific content pipelines for Twitter, LinkedIn, and Instagram |
| 05 | **Research and Write Article** | Sequential crew: Content Planner → Writer → Editor |
| 06 | **Customer Support Automation** | Support agent with QA specialist and delegation |
| 07 | **Customer Outreach Campaign** | Lead profiling with DirectoryReadTool, FileReadTool, custom SentimentAnalysisTool |
| 08 | **Automate Event Planning** | Venue, logistics, and marketing agents with async execution and human-in-the-loop |
| 09 | **Financial Analysis Collaboration** | Multi-agent trading workflow: Data Analyst → Strategy Developer → Trade Advisor → Risk Advisor |
| 10 | **Tailor Job Applications** | Resume tailoring with MDXSearchTool, FileReadTool, and scraping |

### CrewAI Patterns Covered

| Pattern | Projects |
|---------|----------|
| Sequential crews | 02, 04, 05, 06, 07, 08, 09, 10 |
| CrewAI Flows (`@start`, `@listen`, `@router`) | 01 (Dynamic Travel Advisor) |
| ConditionalTask | 01 (Fraud Detection) |
| Custom tools (`BaseTool`) | 01 (DownloadImageTool, EmailGeneratorTool), 07 (SentimentAnalysisTool) |
| Pydantic structured output | 01, 02, 03, 08 |
| Memory (Mem0) | 01 (Book Recommendation) |
| CodeInterpreterTool | 01 (Data Analyst) |
| DALL-E image generation | 01 (Image Generation) |
| Async execution | 01 (Employee Onboarding), 03, 08 |
| Human-in-the-loop | 08 (Event Planning) |
| Agent delegation | 06, 09 |
| Hierarchical process | 01 (Document Summarization) |
| Custom LLM config per agent | 01 (Document Summarization) |
| Databricks Apps deployment | 03 (Mock Interviewer) |
| Web search & scraping | 01–10 (SerperDevTool, ScrapeWebsiteTool, WebsiteSearchTool) |

### 01. Some Simple AI Agents — Details

| Notebook | Focus |
|----------|-------|
| `1. Fitness_Progress_Tracker` | Web search with SerperDevTool for fitness plans |
| `2. Dynamic_Travel_Advisor` | CrewAI Flows — validation, routing, state management |
| `3. Advanced_Images_Generation` | Prompt improvement + DALL-E + custom DownloadImageTool |
| `4. Personalized_Book_Recommendation` | Mem0 memory integration with `memory_config` |
| `5. Data_Analyst_Agent` | CodeInterpreterTool for Python data analysis |
| `6. Fraud_Detection` | ConditionalTask with Pydantic output and escalation logic |
| `7. Employee_Onboarding_Workflow` | Custom EmailGeneratorTool and async crews |
| `8. Automated_Document_Summarization` | Hierarchical process with FileReadTool and per-agent LLM configs |

### 03. Multi-Agent Mock Interviewer — Details

A full-stack interview preparation system deployed on Databricks Apps.

**Agents:** Company Research Specialist, Q&A Preparer, Answer Evaluator, Follow-up Question Specialist, New Topic Question Specialist

**Architecture:**
1. **Preparation crew** — company research → question generation (Pydantic `QuestionAnswerPair`)
2. **Evaluation crew** — evaluates the user's answer
3. **Follow-up crew** — generates follow-up or new-topic questions

| File | Purpose |
|------|---------|
| `interview_practice_system.py` | CrewAI agent and crew logic |
| `chatbot_ui.py` | Streamlit conversational UI |
| `app.yaml` | Databricks Apps configuration |
| `databricks.yml` | Databricks Asset Bundles |

**Technologies:** CrewAI 0.114+, Streamlit, Whisper, Pydantic, Databricks Apps

**Dependencies:** `crewai[tools]>=0.114.0`, `streamlit>=1.44.1`, `streamlit-mic-recorder`, `openai-whisper`

---

## Technologies & Libraries

| Category | Technologies |
|----------|-------------|
| **Agent Frameworks** | Microsoft AutoGen, CrewAI |
| **LLM Providers** | OpenAI (GPT-3.5-turbo, GPT-4, GPT-4o-mini, GPT-4.1-nano), Groq (Llama 3.3 70B) |
| **Vector Database** | ChromaDB |
| **Memory** | Mem0 |
| **Finance Data** | yfinance |
| **Web Search** | SerperDevTool |
| **Image Generation** | DALL-E |
| **Speech-to-Text** | OpenAI Whisper |
| **Web UI** | Streamlit |
| **Deployment** | Databricks Apps, Databricks Asset Bundles |
| **Configuration** | python-dotenv, JSON config files, YAML |

## Getting Started

1. **Clone the repository**

2. **Set up environment variables** — create a `.env` file with your API keys:

```
OPENAI_API_KEY=your-openai-key
GROQ_API_KEY=your-groq-key
SERPER_API_KEY=your-serper-key
```

3. **Install dependencies** — each project folder may have its own `requirements.txt` or `pyproject.toml`:

```bash
# AutoGen projects
pip install -r "Projects with Autogen/0. Some Simple Agents/requirements.txt"
pip install -r "Projects with Autogen/5. Stock Market Analysis Agent/requirements.txt"

# CrewAI projects
pip install -r "Projects with CrewAI/03. Building a Multi-Agent AI-Powered Mock Interviewer using CrewAI/requirements.txt"
```

4. **Run notebooks** with Jupyter, or launch Streamlit apps:

```bash
# AutoGen Streamlit app
cd "Projects with Autogen/5. Stock Market Analysis Agent"
streamlit run app.py

# CrewAI Mock Interviewer
cd "Projects with CrewAI/03. Building a Multi-Agent AI-Powered Mock Interviewer using CrewAI"
streamlit run chatbot_ui.py
```

## License

This project is licensed under the [Apache License 2.0](LICENSE).
