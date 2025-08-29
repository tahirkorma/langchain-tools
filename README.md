# LangChain Tools

This repository demonstrates how to use **LangChain Tools** – both built-in and custom – to extend the functionality of language models. Tools allow LLMs to **interact with external systems** such as search engines, APIs, databases, or even the local shell, making them more practical and powerful.

---

## 📌 Tools in LangChain

### 🔹 Built-in Tools
LangChain comes with a variety of prebuilt tools that can be used out of the box:
- **DuckDuckGo Search Tool** – enables LLMs to fetch real-time search results from the web.
- **Shell Tool** – executes shell commands directly from within an agent.

### 🔹 Custom Tools
You can also create your own tools to suit specific needs:
- **@tool decorator (`langchain_community.tools import tool`)** – simple way to wrap Python functions as LangChain tools.  
- **StructuredTool (with `pydantic` models)** – allows defining structured input and validation using `BaseModel` and `Field`.  
- **BaseTool (`langchain.tools import BaseTool`)** – the most flexible way to build custom tools by subclassing and implementing specific logic.

---

## ⚙️ Concepts in Tool Usage

- **Toolkit** – a collection of tools bundled together that an agent can use.  
- **Tool Binding** – the process of associating a specific function or API with a tool definition.  
- **Tool Calling** – the LLM decides when to invoke a tool during reasoning.  
- **Tool Execution** – the actual running of the tool, returning results back to the LLM.  
- **AgentExecutor** – orchestrates the interaction loop between the LLM, the tools, and the user prompt.

---

## 💱 Project: Currency Conversion Tool

This project demonstrates how to build and use custom tools with LangChain by implementing a **Currency Conversion Agent**.

### 🔹 How It Works
1. **User Input** – The user provides two currencies and an amount.  
2. **Tool 1: Fetch Conversion Rate** – A tool queries an API (Exchange Rate API) to get the exchange rate between the two currencies.  
3. **Tool 2: Multiply Conversion** – A simple tool multiplies the rate with the user’s input amount to calculate the converted value.  
4. **AgentExecutor** – manages the reasoning flow, ensuring the right tools are called in the right sequence.  

This setup showcases how **multiple tools can be combined** to solve a practical task.
