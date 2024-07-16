# Chat with PDF using Gemini 💁

This project is a Streamlit application that allows users to upload PDF files and interact with them by asking questions. The application utilizes Google Generative AI models for embeddings and conversational AI.

## Features

- Upload multiple PDF files
- Extract text from PDF files
- Split text into manageable chunks
- Create and store embeddings using Google Generative AI models
- Perform similarity search on the text chunks
- Answer questions based on the extracted text using Google Generative AI conversational model

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/chat-pdf-gemini.git
    cd chat-pdf-gemini
    ```

2. Create a virtual environment and activate it:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Set up your environment variables:
    - Create a `.env` file in the root directory of your project.
    - Add your Google API key to the `.env` file:
      ```plaintext
      GOOGLE_API_KEY=your_google_api_key_here
      ```

## Usage

1. Run the Streamlit application:
    ```bash
    streamlit run app.py
    ```

2. Open the Streamlit app in your browser. You can typically find it at `http://localhost:8501`.

3. Upload your PDF files using the sidebar.

4. Ask questions in the main interface after uploading and processing the PDFs.

## Code Overview

- `app.py`: Main application file that contains the Streamlit app.
- `requirements.txt`: List of dependencies required for the project.
- `.env`: Environment variables file to store your Google API key.

### Main Functions

- `get_pdf_text(pdf_docs)`: Extracts text from the uploaded PDF files.
- `get_text_chunks(text)`: Splits the extracted text into chunks.
- `get_vector_store(text_chunks)`: Creates and stores embeddings for the text chunks using FAISS.
- `get_conversational_chain()`: Sets up the conversational AI model using Google Generative AI.
- `user_input(user_question)`: Handles user questions and returns responses based on the context of the uploaded PDFs.

## Requirements

- Python 3.7 or higher
- [Streamlit](https://streamlit.io/)
- [PyPDF2](https://pypi.org/project/PyPDF2/)
- [LangChain](https://github.com/hwchase17/langchain)
- [google-generativeai](https://pypi.org/project/google-generativeai/)
- [FAISS](https://github.com/facebookresearch/faiss)
- [python-dotenv](https://github.com/theskumar/python-dotenv)

