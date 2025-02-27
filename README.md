# Essay-Writer-with-Interface-GUI
## Essay Writer Using Agent
To get started with the Essay Writer Using Agent, follow these steps:

## Set up virtual environment and install dependencies

python3 -m venv venv
source venv/bin/activate  

## On Windows use `venv\Scripts\activate`
pip install -r requirements.txt

## Create and configure the .env file Create a .env file in the root directory and assign the necessary API keys:

OPENAI_API_KEY=sk-....
TAVILY_API_KEY=tvly-.....

## Run the application

python app.py

# Multi-agent designs
Focused Tools: Grouping tools by responsibility enhances performance as agents perform better with focused tasks than when choosing from many tools.
Separate Prompts: Using distinct prompts with specific instructions and examples improves results. Each agent can even use a separate fine-tuned LLM.
Modular Development: Evaluating and improving each agent individually is easier and doesn't affect the larger application.
Divide and Conquer: Multi-agent designs break complex problems into manageable tasks, allowing specialized agents and LLM programs to target each unit effectively.
Agent Connection
The router primarily manages state transitions. After each LLM call, it examines the output. If a tool is invoked, it calls that tool. If the LLM responds with "FINAL ANSWER," it returns the response to the user. If neither condition is met, it passes the task to another LLM.

![image](https://github.com/user-attachments/assets/ab1f825e-df1b-4758-8d45-a1182bf834ba)

## References:
[LangGraph Documentation
](https://blog.langchain.dev/langgraph/)
[LangGraph: Multi-Agent Workflows](https://blog.langchain.dev/langgraph-multi-agent-workflows/)
[Adaptive RAG
](https://langchain-ai.github.io/langgraph/tutorials/rag/langgraph_adaptive_rag/)
[CrewAI Documentation
](https://docs.crewai.com/introduction)
[GPTResearcher Github](https://github.com/assafelovic/gpt-researcher?ref=blog.langchain.dev)
