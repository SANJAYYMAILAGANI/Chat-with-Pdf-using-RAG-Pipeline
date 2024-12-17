# Chat-with-Pdf-using-RAG-Pipeline
The goal is to implement a Retrieval-Augmented Generation (RAG) pipeline for interacting with semi-structured data in multiple PDF files. The system will extract relevant information from these files, segment it into manageable chunks, and convert these chunks into embeddings for efficient retrieval.

This solution implements a Retrieval-Augmented Generation (RAG) pipeline to interact with semi-structured data from PDF files. Here's a brief breakdown of the process:

Data Ingestion: The text from a PDF is extracted, split into manageable chunks (e.g., sentences), and processed for embedding.

Embedding and Storage: Each text chunk is converted into vector embeddings using a SentenceTransformer model. These embeddings are stored in a FAISS index, allowing for fast and efficient similarity-based retrieval.

Query Handling: When a user submits a query, the system converts the query into an embedding, retrieves the most relevant text chunks from the FAISS index, and displays them.

Comparison Queries: If the query asks for comparisons (e.g., data from tables), the system extracts tabular data using regular expressions and displays it in a readable format using Pandas.

User Interaction: The system continuously prompts the user for queries, handling both normal and comparison queries, and outputs relevant data or extracted tables as needed.

This pipeline allows efficient, local interaction with PDF-based data without needing external APIs, offering a scalable solution for document-based queries.






