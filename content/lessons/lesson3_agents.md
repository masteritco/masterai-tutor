
---

### 📘 `lesson3_agents.md` — *What is an AI Agent?*

```markdown
# Lesson 3: What is an AI Agent?

### 🤖 What is an AI Agent?

An **AI Agent** is a smart assistant that:
- Uses an LLM (like GPT) as a brain
- Has tools (search, calculator, API access)
- Makes decisions based on goals and responses

You can think of it as a **digital intern** who can search, summarize, email, and more.

---

### 🧪 LangChain Agent Example

```python
from langchain.agents import initialize_agent, load_tools
from langchain.chat_models import ChatOpenAI

llm = ChatOpenAI(temperature=0)

tools = load_tools(["serpapi", "llm-math"], llm=llm)

agent = initialize_agent(
    tools,
    llm,
    agent="zero-shot-react-description",
    verbose=True
)

agent.run("What's the current weather in Paris?")
