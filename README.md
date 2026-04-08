Overview

This project implements a Retrieval-Augmented Generation (RAG) Chatbot that answers questions based on a research paper:

“AI Ethics: Integrating Transparency, Fairness, and Privacy in AI Development” by Petar Radanliev

The chatbot combines:

 Document understanding (PDF ingestion)
 Semantic search (vector embeddings)
 LLM-based responses (Mistral AI)
 Memory for conversational context

The goal is to build an ethical AI assistant that explains concepts like:

Transparency
Fairness
Privacy
Global AI policy frameworks
 Key Features

 Upload and process research PDFs
 Chunking using Recursive Text Splitter
 Semantic embeddings using Google Gemini
 Vector storage and retrieval
 Conversational QA using LLM (Mistral) 
 Context-aware responses with memory
 Focus on AI Ethics and Governance

 Architecture

The system follows a modular RAG pipeline:

PDF → Text Splitter → Embeddings → Vector Store → Retriever → LLM → Chatbot UI
 Components Used
Component	Purpose
Recursive Character Text Splitter	Breaks document into chunks
File Loader	Loads PDF
Google Gemini Embeddings	Converts text to vectors
In-Memory Vector Store	Stores embeddings
Retriever	Fetches relevant chunks
Mistral AI Model	Generates answers
Buffer Memory	Maintains conversation
Conversational Retrieval QA Chain	Connects everything
<img width="1847" height="873" alt="rag" src="https://github.com/user-attachments/assets/7a56a29c-92b0-4df0-a48f-c1308ac6a9b7" />

 Workflow Explanation
Document Upload
Research paper is uploaded and parsed
Text Chunking
Large text is split into smaller chunks for better retrieval
Embedding Generation
Each chunk is converted into vector representation
Storage
Stored in an in-memory vector database
User Query
User asks a question via chatbot UI
Retrieval
Relevant chunks are fetched using similarity search
LLM Response
Mistral model generates contextual answer
Memory Handling
Previous conversation is used for better responses
About the Research Paper

The chatbot is built on a research paper that highlights:

 Core Ethical Principles
Transparency → AI decisions should be explainable
Fairness → Avoid bias and discrimination
Privacy → Protect user data
 Global Framework Comparison

The paper compares AI policies from:

European Union
United States
China
 Key Challenges
Bias in AI systems
Lack of global standards
Trade-offs between innovation and regulation
 Proposed Solutions
Fairness-aware algorithms
Regular audits
Diverse development teams
Ethical AI lifecycle integration
 System Interface

The chatbot UI allows users to:

Ask questions about the document
Get contextual answers
Maintain conversation history

Note:
If you see Ending nodes not found, it means:

The pipeline connections are incomplete
Or the QA chain is not properly linked
 Tech Stack
LLM: Mistral AI
Embeddings: Google Gemini
Framework: RAG (Retrieval-Augmented Generation)
Vector Store: In-Memory
UI: Visual pipeline builder (node-based)
Setup Instructions
1. Clone Repository
git clone https://github.com/your-username/ai-ethics-rag-chatbot.git
cd ai-ethics-rag-chatbot
2. Add API Keys
Mistral API Key
Google Generative AI Key
3. Upload Document
Add the AI Ethics PDF
4. Connect Pipeline Nodes

Ensure:

Retriever → QA Chain
LLM → QA Chain
Memory → QA Chain
5. Run Chatbot
Start the pipeline
Ask questions
 Example Questions
What is AI ethics?
Explain transparency in AI
What are global AI frameworks?
How can bias be reduced in AI systems?
Compare EU and US AI policies
 Common Errors & Fixes
 "Ending nodes not found"

 Fix:

Connect all nodes properly
Ensure QA chain has:
LLM
Retriever
Memory
 No response from chatbot

 Fix:

Check API keys
Verify embeddings are generated
Ensure document is loaded
 Future Improvements
Persistent vector database (FAISS / Pinecone)
Multi-document support
UI enhancements
Real-time policy updates
Advanced explainability features
 Contributing

Contributions are welcome!
Feel free to:

Improve pipeline
Add new features
Optimize performance
 License

This project is for educational and research purposes.

 Author
Sakshi 
