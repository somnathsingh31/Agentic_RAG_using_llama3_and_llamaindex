# Agentic RAG Using LLaMa3 and LlamaIndex

## Overview

This project implements an Agentic Retrieval-Augmented Generation (RAG) system using the LLaMa-3 model and the LlamaIndex library. The system combines powerful language models with advanced querying capabilities to provide accurate and contextually relevant answers. The project focuses on integrating tools and agents to enhance the interaction between language models and specific datasets.

## Features

- **LLaMa-3 Integration**: Utilizes the Meta-LLaMa-3-8B-Instruct model for natural language processing tasks.
- **LlamaIndex**: Provides efficient vector-based document retrieval.
- **Agentic RAG**: Employs a ReAct agent for advanced decision-making and tool usage.
- **Custom Tools**: Includes basic arithmetic tools and RAG-based query engines for specific domains.

## Setup

### Requirements

- Python 3.8+
- LLaMa-3 model
- Hugging Face API Key

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/somnathsingh31/Agentic_RAG_using_llama3_and_llamaindex.git
   cd agentic-rag
   ```

### Usage

1. Load your data:

   ```python
   from llama_index.core import SimpleDirectoryReader
   documents = SimpleDirectoryReader(input_files=["/path/to/your/documents.pdf"]).load_data()
   ```

2. Create and configure the RAG system:

   ```python
   from llama_index.core import VectorStoreIndex
   index = VectorStoreIndex.from_documents(documents)
   query_engine = index.as_query_engine(similarity_top_k=3)
   ```

3. Query the system:

   ```python
   response = query_engine.query("What is the feature of the product?")
   print(response)
   ```

### Example

Here’s a basic example of querying the system:

```python
response = agent.chat("What is special about Jio Meet?")
print(response)
```

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

### Acknowledgments

- Meta for providing the LLaMa-3 model
- LlamaIndex for their advanced document retrieval library
- Hugging Face for their model hosting and API services
