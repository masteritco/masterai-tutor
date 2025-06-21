# Lesson 2: What is LangChain?

### 🧠 What is LangChain?

**LangChain** is a Python (and JavaScript) framework for building apps powered by LLMs like GPT-4. It helps developers:

- Add memory to AI apps
- Connect LLMs with tools (Google Search, APIs)
- Create multi-step workflows (agents)
- Manage conversations

---

### 🧪 LangChain Code Example: Simple Chat with Memory

```python
from langchain.chat_models import ChatOpenAI
from langchain.chains import ConversationChain
from langchain.memory import ConversationBufferMemory

llm = ChatOpenAI(temperature=0.7)

conversation = ConversationChain(
    llm=llm,
    memory=ConversationBufferMemory()
)

response = conversation.predict(input="Tell me a fun fact about space.")
print(response)
