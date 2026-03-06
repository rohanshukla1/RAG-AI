# Project 1: RAG App (Retrieval Augmented Generation)

## What is RAG?

RAG (Retrieval Augmented Generation) is a technique that allows AI to answer questions using your own documents. Instead of relying only on training data, the AI retrieves relevant information from your documents and uses it to generate accurate answers.

This project builds a simple **RAG system using Python and OpenAI** that can read documents and answer questions about them.

---

# What You'll Learn

* How to load and process text documents
* Creating embeddings (numerical representations of text)
* Searching for relevant information
* Combining retrieval with AI generation
* Building a basic AI document assistant

---

# Prerequisites

Before starting, make sure you have:

* Python **3.8 or higher**
* **pip** installed
* An **OpenAI API Key**

Get an API key here:
https://platform.openai.com

---

# Project Structure

Your project should look like this:

```
RAG-App/
│
├── rag_app.py
├── requirements.txt
├── README.md
├── .env
└── documents/
      sample.txt
```

---

# Step 1: Install Dependencies

Open terminal inside the project folder and run:

```bash
pip install -r requirements.txt
```

This installs all required Python libraries.

---

# Step 2: Set Up Your API Key

Create a file named **.env** in the project folder.

Example:

```
.env
```

Inside the file add:

```
OPENAI_API_KEY=sk-your-api-key-here
```

Replace `sk-your-api-key-here` with your actual OpenAI API key.

---

# Step 3: Add Documents

Create a folder named:

```
documents
```

Add your **text files (.txt)** inside this folder.

Example:

```
documents/
    sample.txt
    notes.txt
    report.txt
```

The AI will use these files to answer questions.

---

# Step 4: Run the Application

Run the program using:

```bash
python rag_app.py
```

The app will:

1. Load documents
2. Split them into chunks
3. Create embeddings
4. Store vectors
5. Start the question interface

---

# Step 5: Ask Questions

Once the app starts, you can ask questions like:

```
What is written in sample.txt?
Summarize the document.
Explain the main topic.
```

The system will search the documents and generate answers.

---

# How It Works

### 1. Load Documents

Reads text files from the **documents folder**.

### 2. Text Splitting

Large documents are split into smaller chunks for better processing.

### 3. Create Embeddings

Text chunks are converted into **vector embeddings**.

### 4. Store Vectors

Embeddings are stored to allow fast similarity searches.

### 5. Query

When a user asks a question, the system finds relevant document chunks.

### 6. Generate Answer

The AI generates an answer using retrieved information.

---

# Files in This Project

| File             | Description                  |
| ---------------- | ---------------------------- |
| rag_app.py       | Main application script      |
| requirements.txt | Python dependencies          |
| documents/       | Folder containing text files |
| .env             | Stores the OpenAI API key    |
| README.md        | Project documentation        |

---

# Tips for Beginners

* Start with **small text files**
* Ask **specific questions**
* Clean and structured documents give better answers
* Try adding multiple documents

---

# Common Issues

### No Documents Found

Make sure `.txt` files are placed inside the **documents folder**.

### API Key Error

Ensure the `.env` file contains:

```
OPENAI_API_KEY=sk-your-api-key
```

### Slow Processing

Large documents take more time to process.

---

# Future Improvements

You can upgrade this project by adding:

* PDF support
* Excel and Word document support
* Vector databases like **FAISS or Chroma**
* Web UI (Streamlit or React)
* Multi-document chat system
* Memory-based conversations

---

# Conclusion

This project demonstrates how to build a **basic Retrieval Augmented Generation (RAG) system** that can analyze documents and answer questions based on them.

It is a great starting point for building **private AI assistants, document analyzers, and knowledge base systems**.
