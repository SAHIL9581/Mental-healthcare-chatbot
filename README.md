# 🧠 Mental Health Chatbot

A compassionate AI-powered chatbot built to provide mental health support and guidance. This project uses LangChain, Groq LLM (Llama-3.3-70b-versatile), and RAG (Retrieval-Augmented Generation) to deliver context-aware responses from a custom knowledge base of mental health resources.

## 📝 Features

- **Context-Aware Responses**: Uses RAG to retrieve relevant information from mental health PDFs
- **LLM Integration**: Powered by Groq's Llama-3.3-70b-versatile model
- **Vector Database**: ChromaDB for efficient semantic search of document chunks
- **Gradio Interface**: Clean, user-friendly web interface
- **Custom Prompt Engineering**: Designed to provide compassionate and thoughtful responses

## 🛠️ Technologies Used

- **LangChain**: For building the RAG pipeline and LLM integration
- **Groq**: API for accessing the Llama-3.3-70b model
- **ChromaDB**: Vector database for document storage and retrieval
- **HuggingFace Embeddings**: Sentence-transformers/all-MiniLM-L6-v2 for document embeddings
- **PyPDF**: For loading and processing PDF documents
- **Gradio**: For creating the web interface

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Groq API key

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mental-health-chatbot.git
   cd mental-health-chatbot
   ```

2. Install the required packages:
   ```bash
   pip install langchain_groq langchain_core langchain_community pypdf chromadb sentence_transformers gradio
   ```

3. Set up your Groq API key:
   ```python
   # Replace this in the code with your own Groq API key
   groq_api_key = "your_groq_api_key_here"
   ```

4. Prepare your data:
   - Create a folder named `data` in the project directory
   - Add PDF files with mental health information to this folder

### Running the Application

#### Command Line Interface
```python
python main.py
```

#### Web Interface
```python
python gradio_app.py
```

## 📊 Project Structure

```
mental-health-chatbot/
├── main.py                # Command-line version of the chatbot
├── gradio_app.py          # Web interface version
├── data/                  # Directory for PDF documents
│   └── *.pdf              # Your mental health PDF resources
├── chroma_db/             # Vector database storage (created automatically)
└── README.md              # This file
```

## 💡 How It Works

1. **Document Processing**: PDF files are loaded and split into smaller chunks
2. **Embedding Generation**: Each chunk is converted into a vector embedding
3. **Vector Storage**: Embeddings are stored in a ChromaDB database
4. **Query Processing**: User questions are converted to embeddings and semantically similar documents are retrieved
5. **Context-Enhanced Response**: Retrieved documents are provided as context to the LLM, which generates a thoughtful response

## 🎨 Customization

You can customize the chatbot's behavior by modifying the prompt template:

```python
prompt_template = """You are a compassionate mental health chatbot. Respond thoughtfully.

{context}
User: {question}
Chatbot:"""
```

## 🔒 Privacy Note

This chatbot does not store conversation history on the server side. All interactions are processed in real-time and not saved.

## ⚠️ Disclaimer

This chatbot is for informational purposes only and is not a substitute for professional mental health services. If you're experiencing a mental health crisis, please contact a qualified healthcare provider or a crisis helpline.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
