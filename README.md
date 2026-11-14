# Multi-Agent AI Research System

A multi-stage research workflow built with **LangChain and LangGraph**: you give it a query, and specialised agents search the web, read pages, write a report, and critique it.

## How it works
```
Query → Search Agent (Tavily) → Reader Agent → Writer Chain → Critic Chain → Final report
```
- **Search Agent:** retrieves web results via Tavily
- **Reader Agent:** extracts the relevant content from the pages
- **Writer Chain:** generates the research report from the extracted content
- **Critic Chain:** evaluates the report and supports feedback
- Source-backed output, exported as Markdown through a Streamlit interface
- LLM: OpenAI GPT-4o-mini

## Tech stack
Python, LangChain, LangGraph, Streamlit, Tavily, OpenAI GPT-4o-mini

## Run locally
```bash
git clone https://github.com/jayant13042004/multi-agent-research-system.git
cd multi-agent-research-system
pip install -r requirements.txt
cp .env.example .env      # add OPENAI_API_KEY and TAVILY_API_KEY
streamlit run [app_file].py
```

## Demo
(Add a screenshot or short GIF: `![demo](images/demo.png)`)
Add one sample query and the generated report under `examples/`.

## Limitations
- Report quality depends on search results and the underlying LLM.
- No automated evaluation yet; outputs are judged manually.

## Author
Jayant Jagtap · [LinkedIn](https://www.linkedin.com/in/jayantjagtap/)
