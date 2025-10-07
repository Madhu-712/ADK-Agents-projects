# Personal Assistant Agent (built with ADK)

This project contains a simple personal assistant agent built using the Google Agent Development Kit (ADK). This agent is based on the "Building AI Agents with ADK: The Foundation" codelab.

## Codelab Reference

For more detailed information, please refer to the official codelab:
[Building AI Agents with ADK: The Foundation](https://codelabs.developers.google.com/devsite/codelabs/build-agents-with-adk-foundation?hl=en)

## Setup and Execution

### 1. Configure Google Cloud Services (Codelab Section 3)

This project requires Google Cloud services to function.

1.  **Create or select a Google Cloud project.**
2.  **Enable the Vertex AI API:**
    ```bash
    gcloud services enable aiplatform.googleapis.com
    ```
3.  **Set environment variables** for your project ID and location. Open your `~/.bashrc` or `~/.zshrc` file and add the following lines, replacing the placeholder values with your actual project ID and desired location:
    ```bash
    export GOOGLE_CLOUD_PROJECT="<your-gcp-project-id>"
    export GOOGLE_CLOUD_LOCATION="<your-gcp-location>"
    ```
    Then, source the file (e.g., `source ~/.bashrc`).

### 2. Create a Python Virtual Environment (Codelab Section 4)

It is recommended to use a Python virtual environment.

1.  **Create a virtual environment:**
    ```bash
    python -m venv .venv
    ```
2.  **Activate the virtual environment:**
    ```bash
    source .venv/bin/activate
    ```
3.  **Install the `google-adk` library:**
    ```bash
    pip install google-adk
    ```

### 3. Create Your First Agent (Codelab Section 5)

The agent is defined by the files in this project.

-   `agent.py`: Defines the agent's logic and configuration.
-   `.env`: Can be used to store environment variables (though the codelab recommends setting them in your shell profile).
-   `__init__.py`: Initializes the Python module.

### 4. Run Your Agent (Codelab Section 6)

You can run the agent directly in your terminal.

```bash
python agent.py
```

### 5. Test and Debug with the ADK Web UI (Codelab Section 7)

The ADK provides a development web UI for an interactive chat experience.

1.  **Run the ADK dev server:**
    ```bash
    adk dev --agent-path .
    ```
2.  **Access the web UI:**
    Open your browser and navigate to the URL provided by the `adk dev` command (usually `http://localhost:8000`).

## About AI Agents and ADK

AI agents leverage Large Language Models (LLMs) to understand, reason, and execute tasks autonomously, acting as personal assistants. The Agent Development Kit (ADK) is a framework from Google that simplifies the process of building and deploying these agents.
