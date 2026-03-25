# Microplastics Research Assistant (RAG System)

An end-to-end retrieval-augmented generation (RAG) system designed to answer questions over a curated corpus of scientific literature on microplastics in environmental and biological systems.

This project demonstrates how LLMs can be combined with vector-based retrieval to generate accurate, context-aware responses grounded in real research papers.

## Features
- PDF ingestion and preprocessing pipeline
- Text chunking and embedding generation
- Vector database retrieval (semantic search)
- Context-aware response generation using LLMs
- Tracing and evaluation with LangSmith
- Iterative optimization of retrieval and generation performance

## How It Works
1. Research papers are ingested and parsed into clean text
2. Documents are split into chunks and converted into embeddings
3. Embeddings are stored in a vector database
4. User queries are embedded and matched against relevant chunks
5. Retrieved context is passed to an LLM to generate grounded responses

## Architecture
PDFs → Chunking → Embeddings → Vector DB → Retrieval → LLM → Answer

## Tech Stack
- Python
- LangChain
- LangSmith (tracing & evaluation)
- OpenAI API (or whichever you used)
- FAISS / Chroma (vector store)
- Pandas / NumPy

## Key Focus Areas
- Retrieval quality and relevance
- Chunking strategy optimization
- Prompt engineering for grounded responses
- Evaluation and debugging of LLM pipelines

## Example Query & Response
**Query:**  
What do the documents say about the effect of microplastics on humans?

**Response:**  
The system synthesizes findings across multiple research papers and indicates that while adverse effects of microplastics on marine organisms are well documented, human health impacts remain less understood. Current evidence is largely based on in-vitro studies, small-scale human studies, and extrapolation from marine biology.

Key findings include:
- Evidence of genotoxicity and cytotoxicity in human cells
- Increased micronucleation and nuclear abnormalities in blood lymphocytes
- Potential links to conditions such as infertility, metabolic disorders, and cardiovascular disease
- Smaller particles (<100 μm) may penetrate biological barriers and accumulate in tissues, including the placenta
- Possible immune responses and toxicity from chemical leaching

Overall, the system highlights that while risks are increasingly recognized, current research is still insufficient to fully quantify human health effects.

**Note:** Responses are generated using retrieved scientific context to ensure grounded, evidence-based answers.