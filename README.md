# Context-Aware LangChain Chatbot

A **context-aware chatbot** built using **LangChain**, **FAISS**, and **HuggingFace Transformers**, deployed in **Google Colab** using **Streamlit** and made accessible via **ngrok**.  

The chatbot can answer questions based on a custom knowledge base (`abc.txt`) and maintain conversation context.

---

## Features

- **Retrieval-based answers** using FAISS vector search  
- **Embeddings** generated with `sentence-transformers`  
- **Language generation** with Flan-T5 model  
- **Context-aware conversation** using LangChain memory  
- **Interactive UI** built with Streamlit  
- **Public URL** for easy access using ngrok  

---

## Libraries & Tools Used

- `langchain` – for conversational retrieval and memory management  
- `faiss` – vector database for semantic search  
- `transformers` – HuggingFace LLM pipelines  
- `sentence-transformers` – for embedding documents  
- `streamlit` – web interface  
- `pyngrok` – expose the Streamlit app publicly  
- `os` & `time` – environment settings and delays  

---

## How It Works

1. **Load Knowledge Base**  
   Load documents from `abc.txt`.

2. **Split Documents**  
   Chunk text into smaller pieces for embedding.

3. **Create Embeddings**  
   Use `sentence-transformers` to generate embeddings for each chunk.

4. **Store in FAISS**  
   Store embeddings in a vector database for fast retrieval.

5. **Set Up LLM**  
   Use the Flan-T5 model to generate natural language answers.

6. **Add Conversational Memory**  
   Track chat history to maintain context during conversations.

7. **Create Retrieval Chain**  
   Combine the LLM, retriever, and memory using LangChain's `ConversationalRetrievalChain`.

8. **Interactive Chat**  
   Users input queries via Streamlit and get context-aware answers.

---

## Example

User: What is LangChain?
Bot: LangChain is a framework for building conversational AI applications using LLMs and retrieval-based techniques.

User: How does FAISS help?
Bot: FAISS stores embeddings and allows fast similarity search to retrieve relevant context for LLMs.
