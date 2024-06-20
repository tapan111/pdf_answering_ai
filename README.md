# pdf_answering_ai
## Here is the streamlit deployed app link- https://pdfansweringai-ufjd5g99a4myf7jdjrfzpb.streamlit.app/
Please Follow instruction.txt for make model to work.
# Chat with Multiple PDFs

This project is a Streamlit-based application that allows users to chat with multiple PDF documents. It uses FAISS for efficient document retrieval and a T5 model for generating responses. The PDF documents are processed, and the text is split into manageable chunks, vectorized, and stored in a FAISS index. Users can then ask questions, and the system retrieves relevant document sections to generate responses.

![image](https://github.com/tapan111/pdf_answering_ai/assets/99003457/86311890-0799-4f90-9c76-41e5837a8001)


## Features

- Upload and process multiple PDF files
- Extract text from PDFs and split it into chunks
- Vectorize text chunks using SentenceTransformers
- Store and retrieve text chunks using FAISS
- Generate responses using a local T5 model
- Interactive chat interface with document preview

## Prerequisites

- Python 3.7 or higher

 Required Python packages (see requirements.txt)

## Installation

1. Clone the repository:
    bash
    git clone https://github.com/tapan111/pdf_answering_ai.git
    cd yourrepository
    

2. Create a virtual environment and activate it:
    bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    

3. Install the required packages:
    bash
    pip install -r requirements.txt
    

4. Download the LaMini-T5-738M model and place it in your project directory:
    - Place the model files in a directory, e.g., models/LaMini-T5-738M

## Usage

1. Run the Streamlit app:
    bash
    streamlit run app.py
    

2. Open your web browser
![image](https://github.com/tapan111/pdf_answering_ai/assets/99003457/4cffa772-e840-4ce4-a1a4-fa0101a9424e)



4. Upload your PDF files using the sidebar, click "Process", and wait for processing to complete.
 ![image](https://github.com/tapan111/pdf_answering_ai/assets/99003457/166e3bd3-0a14-476a-bf52-59ef0dfc20a7)



6. Ask questions about the uploaded documents in the main chat interface.
   Note: Please Download "MBZUAI/LaMini-T5-738M" model from hugging face at your folder location using code from trial.ipynb

## File Structure

- app.py: Main application code.
- Templates.py: HTML and CSS templates for the chat interface.
- requirements.txt: List of required Python packages.

## Code Explanation

### app.py

- *FAISSRetriever Class*: Handles the retrieval of relevant documents from the FAISS index.
- *get_pdf_text*: Extracts text from uploaded PDF files.
- *get_text_chunks*: Splits extracted text into manageable chunks.
- *get_vectorstore*: Vectorizes text chunks and stores them in a FAISS index.
- *get_conversation_model*: Loads the local T5 model for generating responses.
- *generate_response*: Generates a response to the user's query using the T5 model.
- *main*: Streamlit app main function that handles file uploads, processing, and chat interface.

### Templates.py

- *CSS and HTML Templates*: Contains the styles and structure for the chat interface, including user and bot message templates and the PDF preview window.
- *render_pdf*: Function to render PDF files in an iframe for preview.


## Acknowledgements

- [Streamlit](https://streamlit.io/)
- [SentenceTransformers](https://www.sbert.net/)
- [FAISS](https://faiss.ai/)
- [Hugging Face](https://huggingface.co/)


