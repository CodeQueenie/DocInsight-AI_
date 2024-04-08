# DocInsight 🔍

DocInsight is a Streamlit web application designed to extract and analyze information from PDF documents. It utilizes the Gemini Pro model from Google Generative AI to provide conversational question-answering capabilities based on the content of uploaded PDF files.

## Installation

1. Clone this repository to your local machine.
2. Install the required dependencies by running:
```bash
pip install -r requirements.txt
```
3. Set up your Google API key by creating a `.env` file in the project directory and adding your key:
```bash
GOOGLE_API_KEY=your_api_key_here
```

## Usage

To run the application, execute the `main.py` file. The application will launch in your default web browser.

### User Interface

- **Ask a Question**: Enter your question related to the content of the uploaded PDF files.
- **Upload PDF Files**: Select one or more PDF files to upload.
- **Submit & Process**: Initiates the processing of uploaded PDF files and enables answering questions based on the content.

### How It Works

1. **PDF Processing**: Upon uploading PDF files and submitting, the application extracts text from each page of the PDFs and divides it into smaller chunks for efficient processing.
2. **Vectorization**: Text chunks are converted into embeddings using Google Generative AI Embeddings and stored in a FAISS vector store for fast retrieval.
3. **Conversational AI**: The Gemini Pro model is employed for question-answering tasks. It generates responses based on the context provided by the uploaded PDFs and the user's question.
4. **Display Response**: The application displays the generated response to the user's question.

## Dependencies

- Streamlit
- PyPDF2
- langchain
- Google Generative AI
- FAISS
- dotenv

Make sure to install these dependencies before running the application.

## License

This project is licensed under the MIT License. Feel free to use and modify it according to your needs.