# Personal Assistant Agent (built with ADK)

This project contains a simple personal assistant agent built using the Google Agent Development Kit (ADK). This agent is based on the "Building AI Agents with ADK: The Foundation" codelab.

## Project Structure

-   `agent.py`: Defines the agent's logic and configuration, including its name, the Large Language Model (LLM) it uses, and its instructions.
-   `.env`: Stores sensitive configurations like `GOOGLE_CLOUD_PROJECT` and `GOOGLE_CLOUD_LOCATION`.
-   `__init__.py`: Initializes the Python module.

## Setup and Execution

### 1. Environment Setup

It is recommended to use a Python virtual environment. You can create one using `uv`:

```bash
python -m venv .venv
source .venv/bin/activate
```

Install the `google-adk` library:

```bash
pip install google-adk
```

### 2. Google Cloud Integration

This project requires Google Cloud services to function. You will need to:

1.  **Have a Google Cloud project** with billing enabled.
2.  **Enable the `aiplatform.googleapis.com` API.**
3.  **Set up your environment variables** in the `.env` file with your Google Cloud project and location:

    ```
    GOOGLE_CLOUD_PROJECT=<your-gcp-project-id>
    GOOGLE_CLOUD_LOCATION=<your-gcp-location>
    ```

### 3. Running the Agent

You can run the agent in two ways:

*   **In the terminal:**

    ```bash
    python agent.py
    ```

*   **With the development web UI:**
    The ADK provides a development web UI for an interactive chat experience. To use it, you'll need to run the agent with the `adk` command-line tool, which is part of the `google-adk` library.

    ```bash
    adk dev --agent-path .
    ```

    This will start a local web server, and you can interact with your agent in your browser.

## About AI Agents and ADK

AI agents leverage Large Language Models (LLMs) to understand, reason, and execute tasks autonomously, acting as personal assistants. The Agent Development Kit (ADK) is a framework from Google that simplifies the process of building and deploying these agents.
