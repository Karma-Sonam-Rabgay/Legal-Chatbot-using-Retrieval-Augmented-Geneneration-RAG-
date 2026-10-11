# Bangladesh Legal Chatbot Using Retrieval-Augmented Generation (RAG)

## Overview

This project explores the use of Retrieval-Augmented Generation (RAG) to develop a legal information chatbot based on the **Bangladesh Penal Code, 1860**. The chatbot allows users to ask questions about the legal document and receive natural-language answers grounded in relevant retrieved passages.

The system combines document processing, semantic search, and a Large Language Model (LLM) to make legal information easier to access and understand. It was developed using **Google Colab** as part of the CSE299 Junior Design Course at North South University.

## Objectives

- Develop a chatbot that answers questions about the Bangladesh Penal Code, 1860.
- Apply Retrieval-Augmented Generation to ground responses in the uploaded legal document.
- Retrieve relevant passages using semantic similarity search.
- Use a Groq-hosted language model to generate natural-language answers.
- Provide a conversational interface for interacting with the chatbot.

## Key Features

- **PDF-based knowledge source:** Uses the Bangladesh Penal Code, 1860, as the source of legal information.
- **Document processing:** Extracts text from the PDF and divides it into smaller chunks for retrieval.
- **Semantic search:** Uses text embeddings and FAISS to identify relevant document passages.
- **LLM-powered responses:** Uses the Groq API to generate answers based on retrieved information.
- **Conversational interface:** Allows users to ask legal questions through a chat interface.
- **Document-grounded answers:** Designed to avoid unsupported claims when the relevant information is not found in the retrieved passages.

## System Architecture

1. **Document ingestion:** Load and extract text from the Bangladesh Penal Code, 1860 PDF.
2. **Text chunking:** Split the extracted text into smaller, overlapping chunks.
3. **Embedding generation:** Convert text chunks into vector representations using a sentence-transformer model.
4. **Vector indexing:** Store the embeddings in a FAISS vector database.
5. **Retrieval:** Search for passages relevant to the user's question.
6. **Answer generation:** Send the question and retrieved passages to a Groq-hosted LLM.
7. **Chat interface:** Display the generated response to the user.

## Technologies Used

- **Programming Language:** Python
- **Development Environment:** Google Colab
- **RAG Framework:** LangChain
- **PDF Processing:** PyMuPDF / PyPDF, depending on the notebook implementation
- **Embeddings:** `sentence-transformers/all-MiniLM-L6-v2`
- **Vector Database:** FAISS
- **LLM API:** Groq
- **Chat Interface:** Gradio

## Repository Structure

```text
Legal-Chatbot-using-Retrieval-Augmented-Generation-RAG/
├── code/
│   └── Legal_chatbot_RAG.ipynb
├── docs/
│   ├── Bangladesh_The_Penal_Code_1860.pdf
│   └── CSE299_Project_Report_2025.docx
└── README.md
```

## Getting Started

### Prerequisites

- A Google account to use Google Colab
- A Groq API key
- Internet access to install dependencies and access the language model API

### 1. Clone the repository

```bash
git clone https://github.com/Karmaaa7/Legal-Chatbot-using-Retrieval-Augmented-Geneneration-RAG-.git
```

```bash
cd Legal-Chatbot-using-Retrieval-Augmented-Geneneration-RAG-
```

### 2. Open the notebook

Open `code/Legal_chatbot_RAG.ipynb` in Google Colab. You can upload the notebook to Colab or open it from your Google Drive.

### 3. Install dependencies

Run the installation cells in the notebook to install the required Python libraries.

Typical dependencies include:

```python
!pip install -q langchain langchain-community langchain-core langchain-text-splitters
!pip install -q sentence-transformers faiss-cpu pypdf
!pip install -q langchain-huggingface groq gradio
```

### 4. Configure API access

Create a Groq API key through the [Groq Console](https://console.groq.com/keys).

Enter the key securely in Google Colab. Do not hardcode API keys in the notebook or commit them to GitHub.

### 5. Load the legal document

Use the included Bangladesh Penal Code, 1860 PDF or provide the PDF at the path expected by the notebook.

### 6. Run the notebook

Execute the cells in order to process the document, build the FAISS index, initialize the language model, and launch the chatbot interface.

## Limitations

- Responses depend on the quality of text extraction and retrieval.
- The chatbot may omit relevant information if the appropriate passages are not retrieved.
- Generated answers may contain errors or misinterpret legal language.
- The knowledge base is limited to the document used in the project unless additional sources are added.
- The chatbot does not automatically verify subsequent amendments or the current legal status of provisions.

**Disclaimer:** This project is intended for academic and informational purposes only. It does not provide professional legal advice. Users should consult the relevant official legal sources or a qualified legal professional for decisions involving actual legal matters.

## Academic Context

- **Course:** CSE299 — Junior Design Course
- **Institution:** North South University
- **Project:** Bangladesh Legal Chatbot Using Retrieval-Augmented Generation (RAG)
- **Supervisor:** [Mirza Mohammad Lutfe Elahi](https://ece.northsouth.edu/people/lutfe-elahi/)

## Acknowledgements

I would like to express my gratitude to [Mirza Mohammad Lutfe Elahi](https://ece.northsouth.edu/people/lutfe-elahi/) for supervising this project as part of the CSE299 course at North South University.

## Author

**Karma Sonam Rabgay**

GitHub: [Karmaaa7](https://github.com/Karmaaa7)

---

*An academic project exploring document-grounded question answering for legal information using Retrieval-Augmented Generation.*
