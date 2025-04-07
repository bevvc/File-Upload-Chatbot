## File-Upload-Chatbot
This project is a Streamlit-based application that allows users to upload various types of files (.txt, .docx, .pptx, .xlsx) and interact with the content using a chatbot interface powered by OpenAI language model.

## Features

- File upload support for various formats (txt, docx, xlsx, pptx)
- Text extraction and processing from uploaded files
- Conversational interface to query the content of the uploaded file
- Integration with OpenAI's language model for generating responses


## Prerequisites

Before you begin, ensure you have met the following requirements:
- Python 3.7+
- An OpenAI API key


## Installation

1. Clone this repository:

2. Create a virtual environment and activate it:
	'python -m venv venv'
	On windows: 'venv\Scripts\activate'
	On macOS: 'source venv/bin/activate'

3. Install the required packages:
'pip install -r requirements.txt'

4. Set up your OpenAI API key:
- Open the 'app.py' file
- Replace the placeholder API key with your actual OpenAI API key: 
"os.environ["OPENAI_API_KEY"] = "your-api-key-here""


## Usage
1. Run the Streamlit app: 
'streamlit run app.py'

2. Open your web browser and go to the URL provided (usually 'http://localhost:8501')

3. Upload a supported file (.txt, .docx, .pptx, .xlsx) using the file uploader

4. Once the file is processed, you can start asking questions about its content in the chat interface


## How it Works

1. The user uploads a file through the interface
2. The application processes the file based on its type, extracting text content
3. The extracted text is split into smaller chunks and embedded using OpenAI's embedding model
4. The embeddings are stored in a FAISS vector database for efficient retrieval
5. When the user asks a question, the application retrieves relevant text chunks from the vector database
6. The retrieved chunks and the user's question are spent to OpenAI's language model to generate a response
7. The response is displayed to the user in the chat interface


## Contributing

Contributions to this project are welcome. Please fork the repository and submit a pull request with your changes.


## Acknowledgements

- [Streamlit] (https://streamlit.io/) for the web application framework
- [LangChain] (https://github.com/hwchase17/langchain) for the document processing and chat model integration
- [OpenAI] (https://openai.com/) for the language model and embeddings
- [FAISS] (https://github.com/facebookresearch/faiss) for the vector database

