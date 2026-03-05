
# 🤖 **18 July 2025 - Diving into OpenAI Agents SDK** 🤖
Here’s a quick summary of our class today on building smart AI agents\!
~~         ----------------~~
### **💰 What are Tokens & How Do They Affect Price?**
**Tokens** are pieces of words. You pay for AI services based on the number of tokens you use for both your prompts (input) and the AI's answers (output).
  * **Token Counter Tool**: https://platform.openai.com/tokenizer
~~         ----------------~~
### **🧠 Giving Your AI a Context with RAG** 
**RAG (Retrieval-Augmented Generation)** gives your AI a long-term memory by letting it search your own documents to find answers.

  * **Embeddings**: This process turns your text into number lists (vectors), where similar concepts get similar numbers.
  * **Vector Databases**: Special databases (like OpenAI's built-in one or Pinecone) that store these vectors and find the most relevant information for your query instantly.

To create your own Vector Store on OpenAI, go to **Dashboard \> Storage \> Vector Stores**, create database, upload your files, attach, and copy the ID to use with the `FileSearchTool`.
~~         ----------------~~
### **🕵️‍♀️ Tracing & Handoffs**
  * **Tracing**: Lets you see the step-by-step logic your agent uses to find an answer. It's perfect for debugging\! See your traces here: https://platform.openai.com/logs?api=traces
  * **Handoffs** 🤝: This is agent-to-agent teamwork\! One agent can pass a task to another, more specialized agent to get a better result.
~~         ----------------~~
### **🚀 Your Task for the Week** 
Your mission is to **brainstorm an exciting product idea** that uses AI agents. Once you have an idea, start planning and building it\!
~~         ----------------~~
### **📘 Class Resources** 

  * **Google Colab**: https://colab.research.google.com/drive/1BE7dpOcGdLVqW5QIJaSrUrZfxSygMYFk
  * **GitHub Code**: https://github.com/syeda-hoorain-ali/giaic-q3/tree/main/class-11
