# enterprise-ai-agent
Production-ready Google GenAI enterprise assistant workflow built in Google Colab.
# Enterprise AI Agent

A production-ready Google GenAI enterprise assistant workflow built and executed in Google Colab. Developed as part of the technical assessment and training program in partnership with **ITG**.

## Project Overview
This project provides an efficient, robust, and secure AI assistant designed to handle natural language conversations for enterprise employees. It utilizes the modern official Google GenAI SDK (`google-genai`) with native chat memory, system instructions, and secure credential handling.

## Key Features
* **Secure Authentication:** Utilizes Google Colab Secrets to manage API keys safely without hardcoding credentials or exposing project IDs.
* **Modern SDK Integration:** Built using the recommended `google-genai` SDK and `gemini-2.5-flash` model.
* **Production-Grade Class Design:** Clean object-oriented architecture (`EnterpriseAgent`) featuring native chat session memory and robust error handling.
* **Zero Broken Dependencies:** Completely free of mock imports or unhosted local servers (such as Triton or Riva), ensuring seamless execution out-of-the-box in Google Colab.

## Installation & Setup

1. **Open in Google Colab:** Open your notebook environment.
2. **Configure Colab Secrets:** Click on the key icon (`🔑`) on the left sidebar of Google Colab, add a secret named `GEMINI_API_KEY` with your actual API key, and enable notebook access.
3. **Run the Workflow:** Execute the cells sequentially to install dependencies, initialize the client, instantiate the agent, and test queries.

## Usage Example
```python
# Initialize the agent
assistant = EnterpriseAgent()

# Ask a question with built-in conversational memory
response = assistant.ask("Can you summarize the corporate remote work policy?")
print(response)
