# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Google AI course repository exploring the Google AI Development Kit (ADK) and agent-based development with Google's Gemini models. The project includes:

- **day-1a-from-prompt-to-action.ipynb**: A Jupyter notebook with 35 cells demonstrating agent creation and usage patterns using the Google ADK
- **sample-agent/**: A Python package containing a sample agent implementation
- **Google ADK (adk)**: Version 0.0.5 is installed for agent development

## Environment Setup

- **Python Version**: 3.12.12
- **Virtual Environment**: `.venv` directory
- **API Key**: Requires `GOOGLE_API_KEY` in `.env` file for Gemini API access

## Running the Notebook

```bash
# Activate the virtual environment
source .venv/bin/activate

# Run the notebook in Jupyter
jupyter notebook day-1a-from-prompt-to-action.ipynb

# Or run specific cells programmatically
jupyter execute day-1a-from-prompt-to-action.ipynb
```

## Running the Sample Agent

```bash
# Activate the virtual environment
source .venv/bin/activate

# Import and use the agent
python3 -c "from sample_agent import agent; print(agent)"
```

## Key Dependencies

- **adk** (0.0.5): Google AI Development Kit for agent development
- **google-generativeai**: For Gemini model access
- **jupyter**, **ipython**: For notebook execution
- **pydantic**: For data validation in agents

The full dependency list is available in the `.venv` environment.

## Agent Architecture

The project uses the Google ADK's `Agent` class from `google.adk.agents.llm_agent`. The sample agent is configured with:
- **Model**: `gemini-2.5-flash-lite`
- **Name**: `root_agent`
- **Description**: Helpful assistant for user questions
- **Instruction**: Answer user questions to the best of your knowledge

When extending agents, follow the pattern in `sample-agent/agent.py` - instantiate an `Agent` object with appropriate configuration parameters.

## Development Notes

- The `.env` file contains `GOOGLE_API_KEY` and is excluded from version control (listed in `.gitignore`)
- The notebook serves as the primary educational material and working space
- The `sample-agent/` directory demonstrates how to structure agent code as a Python package