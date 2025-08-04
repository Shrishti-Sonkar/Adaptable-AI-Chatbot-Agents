# Adaptable AI Chatbot Agents

A modular, extensible Adaptable AI Chatbot Agents framework built with Streamlit and LangGraph, allowing you to create and interact with multiple AI agents using various LLM providers (OpenAI, Groq, Tavily, etc.) and tools (web search, custom system prompts).

## Features

* **Streamlit-based UI**: Intuitive web interface to configure and run AI agents.
* **Multi-provider support**: Easily switch between OpenAI, Groq, and Tavily LLMs.
* **Customizable system prompts**: Define your own system prompts for each agent.
* **Web search integration**: Enable agent-initiated web searches for up-to-date information.
* **Agent management**: Create, save, and reload multiple agent configurations.

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/AI-Agent.git
   cd AI-Agent
   ```

2. **Set up a Python environment**:

   ```bash
   # Using pipenv
   pipenv install
   pipenv shell

   # OR using venv + pip
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

## Configuration

Create a `.env` file in the project root with your API keys:

```dotenv
OPENAI_API_KEY=your_openai_key_here
GROQ_API_KEY=your_groq_key_here
TAVILY_API_KEY=your_tavily_key_here
```

> **Note**: If you do not use `pipenv`, ensure you uncomment the `load_dotenv()` lines in `ai_agent.py`.

## Usage

Run the Streamlit app:

```bash
streamlit run ai_agent.py
```

1. Open the provided local URL in your browser.
2. Select a **Model Provider** (e.g., OpenAI, Groq).
3. Enter or load a **System Prompt** for your agent.
4. Toggle **Web Search** on/off.
5. Type user queries and interact with your custom AI agent in real-time.

## Project Structure

```
AI-Agent/
├── ai_agent.py          # Main Streamlit application
├── requirements.txt     # Python dependencies
├── .env.example         # Example environment variables file
├── agents/              # Optional: saved agent configurations
└── utils/               # Utility modules for API integration
    ├── groq_client.py
    ├── openai_client.py
    └── tavily_search.py
```

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for enhancements, bug fixes, or new features.

## License

This project is licensed under the [MIT License](LICENSE).
