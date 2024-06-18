# Chat with Multiple PDFs

This project is a Streamlit-based application that allows users to chat with multiple PDF documents. It uses FAISS for efficient document retrieval and a T5 model for generating responses. The PDF documents are processed, and the text is split into manageable chunks, vectorized, and stored in a FAISS index. Users can then ask questions, and the system retrieves relevant document sections to generate responses.

## Features

- Upload and process multiple PDF files
- Extract text from PDFs and split it into chunks
- Vectorize text chunks using SentenceTransformers
- Store and retrieve text chunks using FAISS
- Generate responses using a local T5 model
- Interactive chat interface with document preview

## Prerequisites

- Python 3.7 or higher
- Required Python packages (see `requirements.txt`)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/yourrepository.git
    cd yourrepository
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

4. Download the LaMini-T5-738M model and place it in your project directory:
    - Place the model files in a directory, e.g., `models/LaMini-T5-738M`

## Usage

1. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

2. Open your web browser

3. Upload your PDF files using the sidebar, click "Process", and wait for processing to complete.

4. Ask questions about the uploaded documents in the main chat interface.

## File Structure

- `app.py`: Main application code.
- `Templates.py`: HTML and CSS templates for the chat interface.
- `requirements.txt`: List of required Python packages.

## Code Explanation

### app.py

- **FAISSRetriever Class**: Handles the retrieval of relevant documents from the FAISS index.
- **get_pdf_text**: Extracts text from uploaded PDF files.
- **get_text_chunks**: Splits extracted text into manageable chunks.
- **get_vectorstore**: Vectorizes text chunks and stores them in a FAISS index.
- **get_conversation_model**: Loads the local T5 model for generating responses.
- **generate_response**: Generates a response to the user's query using the T5 model.
- **main**: Streamlit app main function that handles file uploads, processing, and chat interface.

### Templates.py

- **CSS and HTML Templates**: Contains the styles and structure for the chat interface, including user and bot message templates and the PDF preview window.
- **render_pdf**: Function to render PDF files in an iframe for preview.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Streamlit](https://streamlit.io/)
- [SentenceTransformers](https://www.sbert.net/)
- [FAISS](https://faiss.ai/)
- [Hugging Face](https://huggingface.co/)
