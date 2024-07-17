# Project Overview

## Purpose
The project aims to create a chatbot uses RAG(Retrieval Augmented Generation) that interacts with users based on uploaded documents, providing answers and managing conversation history.

## Components and Features

### Environment Setup
- Imports necessary libraries (`panel`, `dotenv`, `openai`, etc.).
- Sets up environment variables from `.env` file, including `OPENAI_API_KEY`.

### Model Initialization
- Chooses an appropriate language model (`gpt-3.5-turbo-0301` or `gpt-3.5-turbo`) based on the current date.

### Vector Store and Embeddings
- Utilizes `Chroma` for vector storage and `OpenAIEmbeddings` for embedding functions.

### Question Answering (QA) Chain
- Sets up a `RetrievalQA` chain for answering questions based on vector similarity search.
- Uses a predefined template (`PromptTemplate`) for generating concise answers.

### Memory Management
- Implements `ConversationBufferMemory` to store and retrieve chat history.

### Conversational Retrieval Chain
- Sets up `ConversationalRetrievalChain` to handle conversational flow using the language model and vector retriever.

### Document Handling
- Defines functions (`load_db`) to load PDF documents, split them into chunks, and create an in-memory search database (`DocArrayInMemorySearch`).

### User Interface (UI)
- Uses `panel` for creating a graphical user interface (GUI).
- Provides interactive elements like file upload (`FileInput`), buttons for loading documents (`Load DB`) and clearing history (`Clear History`), and input for user queries (`TextInput`).

### Dashboard
- Constructs a comprehensive dashboard (`pn.Column`) with multiple tabs (`Tabs`).
- Tabs include sections for conversation (`Conversation`), database interactions (`Database`), chat history (`Chat History`), and configuration (`Configure`).



