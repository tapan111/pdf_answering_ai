# pdf_answering_ai
# Chat with Multiple PDFs

This project is a Streamlit-based application that allows users to interact with multiple PDF documents. Utilizing FAISS for efficient document retrieval and a T5 model for generating responses, this application processes PDF documents, splits the text into manageable chunks, vectorizes the text, and stores it in a FAISS index. Users can then ask questions, and the system retrieves relevant document sections to generate responses.

## Features
- Upload and process multiple PDF files
- Extract text from PDFs and split it into chunks
- Vectorize text chunks using SentenceTransformers
- Store and retrieve text chunks using FAISS
- Generate responses using a local T5 model
- Interactive chat interface with document preview

## Prerequisites
- Python 3.7 or higher

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/Deepak42-y/PDF_ANSWERING_AI.git
   cd PDF_ANSWERING_AI
Create and activate a virtual environment:

sh
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install the required packages:

sh
Copy code
pip install -r requirements.txt
Download the LaMini-T5-738M model and place it in your project directory:

Download the "MBZUAI/LaMini-T5-738M" model from Hugging Face.
Place the model files in a directory, e.g., models/LaMini-T5-738M.
Usage
Run the Streamlit app:

sh
Copy code
streamlit run app.py
Open your web browser and navigate to the Streamlit app:

Upload your PDF files using the sidebar.
Click "Process" and wait for the processing to complete.
Ask questions about the uploaded documents in the main chat interface.
File Structure
app.py: Main application code.
Templates.py: HTML and CSS templates for the chat interface.
requirements.txt: List of required Python packages.
Code Explanation
app.py:

FAISSRetriever Class: Handles the retrieval of relevant documents from the FAISS index.
get_pdf_text: Extracts text from uploaded PDF files.
get_text_chunks: Splits extracted text into manageable chunks.
get_vectorstore: Vectorizes text chunks and stores them in a FAISS index.
get_conversation_model: Loads the local T5 model for generating responses.
generate_response: Generates a response to the user's query using the T5 model.
main: Streamlit app main function that handles file uploads, processing, and chat interface.
Templates.py:

CSS and HTML Templates: Contains the styles and structure for the chat interface, including user and bot message templates and the PDF preview window.
render_pdf: Function to render PDF files in an iframe for preview.
Acknowledgements
Streamlit
SentenceTransformers
FAISS
Hugging Face
