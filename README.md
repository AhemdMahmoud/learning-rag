# learning-rag

# 🧠 LangChain & RAG Examples

This repository contains illustrative examples and mini-projects using [LangChain](https://www.langchain.com/), focusing on prompt engineering, memory management, retrieval-augmented generation (RAG), and integration with various open-source models including Mistral and HuggingFace&Cohere.

---
![image](https://github.com/user-attachments/assets/574118a7-478b-42de-871f-1d57ad9b2ad2)

## 📁 Contents

### 1. `langchain_guide.py`

An extensive walkthrough of LangChain core concepts including:

* Initialization with `mistral-large-latest`
* Prompt formatting and templating
* Chaining techniques: `LLMChain`, `SimpleSequentialChain`, `SequentialChain`, and `MultiPromptChain`
* Output parsing with structured schemas and JSON repair
* Routing input queries dynamically to QA, sentiment, or translation chains
* Real-world examples with customer reviews and jokes

> **Use Case:** Learn how to construct and route between multiple language chains and use structured parsing.

---

### 2. `rag_using_opensource.py`

An end-to-end Retrieval-Augmented Generation (RAG) pipeline using open-source tools:

* PDF ingestion with `PyPDFLoader`
* Text chunking via `RecursiveCharacterTextSplitter`
* Embedding generation using `FastEmbedEmbeddings` (`gte-large`)
* Vector storage using `Chroma`
* Query execution using MMR-based retrieval
* Language model integration via HuggingFace endpoint (`mistralai/Mistral-7B-Instruct-v0.2`)

> **Use Case:** Build lightweight RAG systems using local vectors and open-source LLMs for private document Q\&A.

---
![image](https://github.com/user-attachments/assets/4ce46d5e-329b-4a76-aa99-8359a3639f69)

### 3. `techniques00.py`

Covers various advanced LangChain techniques:

* Prompt engineering with few-shot examples
* Chat simulation with alternating system/user messages
* Memory types: `ConversationBufferMemory`, `BufferWindowMemory`, `SummaryMemory`, and `EntityMemory`
* Output parsers: `CommaSeparatedListOutputParser`, `PydanticOutputParser`
* Saving and reloading chat memory from disk using JSON serialization
* Custom riddles and reasoning examples

> **Use Case:** Understand conversational memory in LangChain and how to persist chat history.

---
![image](https://github.com/user-attachments/assets/7db5396b-186b-4f83-af5b-20da7dae7efd)
## ⚙️ Requirements

Make sure to install the required dependencies:

```bash
pip install langchain langchain-community langchain-huggingface langchain-mistralai fastembed chromadb pypdf
```

For RAG:

```bash
pip install langchain-huggingface
```

---

## 🔑 API Keys

You may need to set the following environment variables depending on which notebooks you use:

```bash
export MISTRAL_API_KEY="your_mistral_key"
export HUGGINGFACEHUB_API_TOKEN="your_huggingface_token"
```

In Google Colab, this is often done via `getpass`.

---

## 🧪 Example Usage

```python
from langchain.prompts import PromptTemplate

template = PromptTemplate.from_template("What is the capital of {country}?")
print(template.format(country="Germany"))
```

---

## 📌 Author

Ahmed Mahmoud

---
