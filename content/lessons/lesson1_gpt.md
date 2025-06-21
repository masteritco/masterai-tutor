# Lesson 1: What is GPT (LLM)?

### 🔍 What is a Large Language Model?

A **Large Language Model (LLM)** is an AI system trained on vast amounts of text to understand and generate human-like language. GPT stands for **Generative Pretrained Transformer**.

OpenAI's GPT-4o is a cutting-edge LLM that can:
- Answer questions
- Generate text, summaries, or emails
- Translate languages
- Write code
- Act as a chatbot or agent

---

### 🧪 Quick Python Example: Use GPT-4o via OpenAI API

```python
import openai

openai.api_key = "your-api-key"

response = openai.ChatCompletion.create(
  model="gpt-4o",
  messages=[
    {"role": "system", "content": "You are a helpful tutor."},
    {"role": "user", "content": "Explain how GPT works in simple terms."}
  ]
)

print(response['choices'][0]['message']['content'])
