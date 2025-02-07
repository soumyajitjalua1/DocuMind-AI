# DocuMind-AI:using deepseek r1


DocuMind AI is an intelligent document assistant that allows users to interact with PDF documents using natural language queries. Built with Streamlit and powered by the Deepseek language model through Ollama, it provides an intuitive interface for document analysis and question-answering.

## Features 🌟

- DF document upload and processing
- Natural language querying of document content
- Real-time AI-powered responses
- Dark mode UI
- Document chunking and semantic search
- Error handling and connection status monitoring

## Prerequisites 🔧

Before running DocuMind AI, ensure you have the following installed:

- ython 3.8 or higher
- Ollama (for running the language model locally)
- Git (for cloning the repository)

## Installation 🚀

1. Clone the repository:

```bash
 git clone https://github.com yourusername/documind-ai.git
 cd documind-ai
```

2. Create and activate a virtual environment:

```bash
 python -m venv venv
.\venv\Scripts\activate

# Linux/MacOS
python3 -m venv venv
source venv/bin/activate
```

3. Install required packages:

-bash

```
pip install -r requirements.txt
```

## Required Packages 📦

Create a requirements.txt file with these dependencies:

```bash
streamlit
langchain
langchain-community
langchain-core
langchain-ollama
pdfplumber
requests
```

## Setting Up Ollama 🤖

1. Install Ollama from ollama.ai
2. Start the Ollama service:

```bash
ollama serve
```

3.Pull the Deepseek model:

```bash
ollama pull deepseek-r1:1.5b
```

## Running the Application 🎯

1. Start the Ollama service and model:

```bash
# Terminal 1
ollama serve

# Terminal 2
ollama run deepseek-r1:1.5b
```

2. Run the Streamlit application:

```bash
streamlit run app.py
```

3. Open your browser and navigate to:

```bash
http://localhost:8501
```

## Usage Guide 📚

- Launch the application and wait for the connection to Ollama to be established
- Upload a PDF document using the file uploader
- wait for the document to be processed
- Type your questions in the chat input
- View AI-generated responses based on the document content

## Project Structure 📁:

```bash
documind-ai/
├── app.py              # Main application file
├── requirements.txt    # Python dependencies
├── document_store/    # Directory for storing uploaded PDFs
│   └── pdfs/
├── README.md          # Project documentation
└── .gitignore        # Git ignore file
```

## Configuration ⚙️

The application uses the following default configuration:

- Ollama endpoint: http://localhost:11434
- PDF storage path: document_store/pdfs/
- Model: deepseek-r1:1.5b
- Chunk size: 1000 characters
- Chunk overlap: 200 characters

## Troubleshooting 🔍

Common Issues and Solutions

1. Ollama Connection Error

- Ensure Ollama is running (ollama serve)
- Check if the model is pulled (ollama pull deepseek-r1:1.5b)
- Verify the endpoint configuration

2. PDF Processing Issues

- Ensure PDF is not password-protected
- Check if the file is corrupted
- Verify write permissions in the document_store directory

3. Memory Issues

- Reduce chunk size for large documents
- Ensure sufficient system RAM
- Close unnecessary applications

## Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

## License 📄

This project is licensed under the MIT License - see the LICENSE file for details.
Acknowledgments 🙏

- Streamlit for the web framework
- LangChain for the document processing pipeline
- Ollama for the local LLM infrastructure
- Deepseek for the language model

## Support 💬

For support, please open an issue in the repository or contact the maintainers.
