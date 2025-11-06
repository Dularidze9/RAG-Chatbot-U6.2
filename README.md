# RAG-Chatbot-U6.2
# რაგ ჩატბოტი-U6.2

This repository contains a conversational AI assistant that blends retrieval-based search with generative models to give informed, context-aware answers.
The system is powered by LangGraph for flow control and LangChain for knowledge access, designed around topics in Computer Science and Natural Language Processing.

# Highlights

 Smart Information Lookup – Retrieves context using hybrid search (semantic + keyword)

 Relevance Filtering – Evaluates retrieved data before generating a response

 Adaptive Workflow – Orchestrated through LangGraph for structured decision-making

 Fallback Awareness – Responds intelligently when context is missing

 Simple Chat UI – Interact instantly through a Gradio interface

# System Breakdown

 Dataset Loader – Imports structured text (e.g., chapters or notes) for indexing

 Vector Indexing – Embeds text via transformer-based encoders and stores in a FAISS database

 Retriever – Combines BM25 with semantic similarity search for better coverage

 Decision Layer – Routes each query through search, web lookup, or fallback modes

 Relevance Evaluation – Ensures that only meaningful context is passed to the generator

 Answer Builder – Produces context-grounded responses using an LLM

 LangGraph Engine – Maintains a multi-step reasoning graph to manage flow

# Setup Instructions

Install dependencies:

pip install langchain langchain-community pypdf sentence-transformers tiktoken rank_bm25 langchain-together tavily-python langgraph gradio faiss-gpu


Configure your API keys:

export TOGETHER_API_KEY="your_key_here"
export TAVILY_API_KEY="your_key_here"


# Run the notebook or script to initialize the workflow and launch the interface.

 Interaction

Start the Gradio app and enter your question.
The model retrieves supporting information, checks relevance, and generates an answer grounded in the material.

 # Disclaimer

This implementation serves learning and research purposes.
It’s a strong foundation for experimentation but would require extra fine-tuning, scalability, and validation for deployment in production.