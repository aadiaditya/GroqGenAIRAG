# RAG Document Q&A with Groq and Llama3

This Streamlit application integrates LangChain with Groq and Llama3 models to provide a Q&A system that retrieves answers from research papers. The app creates vector embeddings from the documents, allowing users to ask questions and get accurate responses based on the context provided in the documents.

## Features

- **Document Embedding**: Load and process research papers to create a vector database.
- **Interactive Q&A**: Ask questions and get answers based on the content of the research papers.
- **Document Similarity Search**: Display similar documents based on the query.

## Setup

### Prerequisites

- Python 3.7 or later
- Streamlit
- LangChain
- OpenAI API Key
- Groq API Key

### Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-repo/rag-document-qa.git
    cd rag-document-qa
    ```

2. **Create a virtual environment**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables**:
    Create a `.env` file in the root directory and add your API keys:
    ```env
    GROQ_API_KEY=your_groq_api_key
    OPENAI_API_KEY=your_openai_api_key
    ```

### Running the App

1. **Start the Streamlit app**:
    ```bash
    streamlit run app.py
    ```

2. **Interact with the Q&A system**:
    - Open the app in your browser (usually at `http://localhost:8501`).
    - Enter your query in the text input.
    - Click "Document Embedding" to create the vector database.
    - Ask questions and view the responses.

## Code Overview

### app.py

This is the main file that sets up the Streamlit app and the LangChain Q&A system.

- **Imports**: Necessary libraries and tools from LangChain and Streamlit.
- **Load Environment Variables**: Load API keys from the `.env` file.
- **Initialize LLM**: Set up the Groq language model.
- **Prompt Template**: Define the template for generating responses.
- **Document Embedding**: Function to create vector embeddings from research papers.
- **Streamlit UI**: Define the main title, user input, and buttons for interaction.
- **Q&A Logic**: Handles user queries, initializes the retrieval chain, and displays the answers.

### Dependencies

- **Streamlit**: For the web interface.
- **LangChain**: For the language model and agent setup.
- **FAISS**: For vector similarity search.
- **dotenv**: For loading environment variables from the `.env` file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [LangChain](https://github.com/langchain-ai/langchain)
- [Streamlit](https://streamlit.io/)
- [Groq](https://groq.com/)
- [OpenAI](https://openai.com/)
