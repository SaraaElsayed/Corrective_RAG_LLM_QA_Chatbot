#Corrective RAG LLM Q&A Chatbot 🤖
Welcome to the Corrective RAG LLM Q&A Chatbot repository! This project is a Retrieval-Augmented Generation (RAG) based chatbot that answers questions by retrieving and refining information from documents and web searches. It uses state-of-the-art language models like Mistral-7B and tools like LangChain, ChromaDB, and Gradio to provide accurate and concise answers.

##Features ✨
Document Retrieval: Extracts and processes information from PDF documents using semantic chunking and vector embeddings.

Knowledge Refinement: Evaluates and refines retrieved documents to ensure relevance and accuracy.

Web Search Integration: Performs web searches to fetch additional context when local knowledge is insufficient.

Interactive Interface: Built with Gradio for a user-friendly chatbot interface.

##Tech Stack 🛠️
Language Model: Mistral-7B-Instruct (mistralai/Mistral-7B-Instruct-v0.3)

Embeddings: GPT4All Embeddings

Vector Database: ChromaDB

Framework: LangChain

Web Search: Tavily Search API

UI: Gradio

Hugging Face Space 🌐
Try the chatbot live on Hugging Face Spaces:
Hugging Face Spaces

##Setup and Installation 🚀
1. Clone the Repository
```bash
$ git clone https://github.com/SaraaElsayed/Corrective_RAG_LLM_QA_Chatbot.git
$ cd Corrective_RAG_LLM_QA_Chatbot
```
2. Install Dependencies
Create a virtual environment and install the required packages:
```bash
$ python -m venv venv
$ source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
$ pip install -r requirements.txt
```
3. Download spaCy Model
Download the en_core_web_sm model for spaCy:
```bash
$ python -m spacy download en_core_web_sm
```
4. Add PDF Files
Place your PDF files (Build a Large Language Model.pdf and Hands-On Large Language Model.pdf) in the root directory of the project.

5. Run the Application
Start the Gradio app:
```bash
$ python app.py
```
The app will be available at http://127.0.0.1:7860

##How It Works 🧠
Document Processing:

PDFs are loaded and split into semantic chunks using SemanticChunker.

Chunks are embedded using GPT4AllEmbeddings and stored in ChromaDB.

Question Answering:

The chatbot retrieves relevant documents from ChromaDB based on the user's question.

It evaluates the relevance of the documents and refines the knowledge if necessary.

If no relevant documents are found, it performs a web search using the Tavily Search API.

Response Generation:

The chatbot generates a concise and accurate answer using the Mistral-7B model.

