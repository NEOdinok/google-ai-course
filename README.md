## Google AI Agents Intensive Course 🚀

Hands-on exploration of the Google AI Development Kit (ADK) and agent-based development with Google's Gemini models.

### 📋 Project Structure

```
google-ai-course/
├── agents/
│   └── sample-agent/          # Sample agent implementation
│       ├── __init__.py
│       ├── agent.py           # Agent definition with root_agent
│       └── .env               # API keys and config
├── day-1a-from-prompt-to-action.ipynb  # Learning notebook
└── .venv/                     # Python virtual environment
```

### ⚙️ Initial Setup

Create and activate a Python 3.12 virtual environment:

```bash
python3.12 -m venv .venv
source .venv/bin/activate
```

### 🏃 Running the ADK Web UI

Start the ADK development server from the project root:

```bash
source .venv/bin/activate
```

```bash
adk web agents
```

Access the UI at `http://127.0.0.1:8000` to interact with your agents.

### 🔧 Important ADK Configuration Notes

**How ADK discovers agents:**
- Expects a parent directory (e.g., `agents/`)
- Each subdirectory is treated as a separate agent
- Each agent requires:
  - `__init__.py` - Must export the agent instance: `from .agent import root_agent`
  - `agent.py` - Must define a `root_agent` variable (not `agent`)
