# ChromaDB Project

This repository uses [ChromaDB](https://www.trychroma.com/) as a vector database for storing and querying embeddings.

## What is ChromaDB?

ChromaDB is an open-source embedding database designed for building AI applications with LLMs. It allows you to store, index, and search high-dimensional vector embeddings efficiently, making it ideal for use cases like:

- Semantic search
- Retrieval-Augmented Generation (RAG)
- Question answering systems
- Recommendation engines

## Features

- Simple Python API
- Local persistence or client-server mode
- Supports metadata filtering alongside vector search
- Integrates easily with LangChain, LlamaIndex, and OpenAI embeddings

## Installation

```bash
pip install chromadb
```

## Basic Usage

```python
import chromadb

client = chromadb.Client()
collection = client.create_collection(name="my_collection")

collection.add(
    documents=["This is a document", "This is another document"],
    ids=["id1", "id2"]
)

results = collection.query(
    query_texts=["This is a query"],
    n_results=2
)

print(results)
```

## License

MIT