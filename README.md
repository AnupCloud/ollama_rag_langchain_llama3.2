# Ollama Llama 3.2 RAG Project

## Overview

This project implements a cutting-edge Retrieval-Augmented Generation (RAG) system utilizing state-of-the-art machine learning models and tools to enhance natural language understanding and response generation.

## 🚀 Project Components
- **Python Version**: 3.12.8
- **Ollama**: A tool for deploying large language models (LLMs)
- **Llama 3.2**: Meta's advanced language model for diverse NLP tasks
- **Chroma DB**: High-performance vector database for embedding storage and retrieval
- **RAG (Retrieval-Augmented Generation)**: Methodology combining pre-trained models with external knowledge sources
- **Streamlit**: Framework for creating interactive web applications

## 📋 Table of Contents

- [Project Components](#-project-components)
- [Installation](#-installation)
- [Usage](#-usage)
- [How RAG Works](#-how-rag-works)
- [Components Explained](#-components-explained)
- [Contributing](#-contributing)
- [License](#-license)

## 🔧 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/AnupCloud/ollama_llama3.2_RAG.git
cd ollama_llama3.2_RAG
```

### 2. Install Python Dependencies

Ensure you have Python 3.7 or later installed:

```bash
pip install -r requirements.txt
```

### 3. Set Up Ollama

Follow the [Ollama Documentation](https://ollama.ai/docs) to set up the platform on your machine.

### 4. Install Chroma DB

```bash
pip install chromadb
```

### 5. Set Up Llama 3.2

Follow instructions from the official Meta website or Ollama's deployment options.

### 6. Install Streamlit

```bash
pip install streamlit
```

## 🚀 Usage

### Example Python Script

```python
from ollama import Ollama
from chromadb import ChromaDB
from rag import RAG

# Initialize components
ollama_model = Ollama(model="llama-3.2")
chroma_db = ChromaDB()
rag = RAG(ollama_model, chroma_db)

# Query and generate response
query = "What are the latest advancements in AI?"
response = rag.get_response(query)

print(response)
```

### Running the Streamlit App

```bash
streamlit run pdf-rag-streamlit.py
```

## 🤖 How RAG Works

RAG (Retrieval-Augmented Generation) combines a retriever (Chroma DB) with a generative model (Llama 3.2):

1. **Input**: User submits a query
2. **Retrieval**: Chroma DB searches for relevant information
3. **Generation**: Llama 3.2 generates a response using query and retrieved context
4. **Output**: Contextually-aware response returned to user

## 📦 Components Explained

### Ollama
A platform for easy deployment of Large Language Models (LLMs) locally or in the cloud.

### Llama 3.2
Meta's state-of-the-art language model designed for:
- Text generation
- Question answering
- Summarization
- Translation

### Chroma DB
A high-performance vector database optimized for:
- Embedding-based search
- Fast information retrieval
- Storing text vectors

### RAG (Retrieval-Augmented Generation)
Enhances language models by:
- Combining generative models with external data sources
- Providing more relevant and up-to-date responses
- Increasing contextual awareness

### Streamlit
An open-source framework for creating interactive web applications, used here to:
- Build a user-friendly interface
- Allow query submission
- Display RAG-generated responses

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Commit and push to your fork
5. Open a pull request with a detailed description

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.