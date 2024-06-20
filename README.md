# pdf_answering_ai
## Here is the streamlit deployed app link- https://pdfansweringai-ufjd5g99a4myf7jdjrfzpb.streamlit.app/
Please Follow instruction.txt for make model to work.
# Chat with Multiple PDFs

his project features a Streamlit-powered application enabling users to interact with numerous PDF files through a chat interface. It utilizes FAISS for optimized document retrieval and employs a T5 model to generate responses. The PDFs undergo processing where their text is segmented into smaller portions, vectorized, and indexed using FAISS. This setup enables users to pose questions, with the system retrieving pertinent sections from the documents to formulate responses.

![image](https://github.com/tapan111/pdf_answering_ai/assets/99003457/86311890-0799-4f90-9c76-41e5837a8001)


## Features

This project facilitates the uploading and processing of multiple PDF files:
Extracts text from PDFs and segments it into manageable chunks.
Utilizes SentenceTransformers to vectorize the text chunks.
Stores and retrieves these vectorized chunks using FAISS.
Employs a local T5 model to generate responses.
Offers an interactive chat interface with previews of the documents.

## Prerequisites

- Python 3.8 or higher

 Required Python packages (see requirements.txt)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/tapan111/pdf_answering_ai.git
    cd yourrepository
    

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    

3. Install the required packages:
    ```bash
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

- bot.py: Main application code.
- Templates.py: HTML and CSS templates for the chat interface.
- requirements.txt: List of required Python packages.

## Code Explanation

### bot.py

- *FAISSRetriever Class*: Manages the retrieval of pertinent documents from the FAISS index.
- *get_pdf_text*: Extracts text from uploaded PDF files.
- *get_text_chunks*: Divides extracted text into manageable segments.
- *get_vectorstore*: Converts text chunks into vectors and stores them within a FAISS index.
- *get_conversation_model*: Loads the local T5 model used for response generation.
- *generate_response*: Utilizes the T5 model to produce responses based on user queries.
- *main*: Central function of the Streamlit app responsible for handling file uploads, processing tasks, and managing the chat interface.

### Templates.py

- *CSS and HTML Templates*: This section encompasses the style definitions and structural elements required for the chat interface. It includes templates for both user and bot messages, as well as the PDF preview window.


## Acknowledgements

- [Streamlit](https://streamlit.io/)
- [SentenceTransformers](https://www.sbert.net/)
- [FAISS](https://faiss.ai/)
- [Hugging Face](https://huggingface.co/)



