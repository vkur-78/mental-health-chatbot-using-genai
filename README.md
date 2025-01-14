# mental-health-chatbot-using-genai


https://github.com/user-attachments/assets/74149870-c06b-4468-8532-9358ed758a89


https://github.com/user-attachments/assets/23183483-bee7-4aef-8c9d-a178b33ef95f


This project demonstrates how to build a chatbot using LangChain, Groq, and Chroma for document retrieval. The bot can answer questions based on information extracted from PDF files. The chatbot uses a custom-trained LLM model (Llama-3.3-70b) powered by Groq's API for processing queries.

## Features

- **LLM Integration:** Uses Groq’s Llama-3.3-70b versatile model.
- **Document Retrieval:** PDF documents are processed to create a vector database using Chroma and HuggingFace embeddings.
- **QA System:** The bot responds to user queries using a RetrievalQA chain that integrates the vector database and LLM.

## Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/chatbot-project.git
   cd chatbot-project
   ```

2. **Install Required Dependencies:**
   Use the following command to install all the necessary libraries:
   ```bash
   pip install -r requirements.txt
   ```
   Alternatively, install them manually:
   ```bash
   pip install langchain_groq langchain_core langchain_community chromadb sentence_transformers huggingface_hub
   ```

3. **Set Up Environment Variables:**
   Create a `.env` file in the project directory and add your Groq API key:
   ```
   GROQ_API_KEY="your_groq_api_key"
   ```

4. **Prepare PDF Data:**
   - Place the PDF documents you want the bot to use in the `data/` folder.

5. **Create Chroma Vector DB:**
   - The vector database is automatically created when the bot is run, by processing the PDF files.

6. **Run the Chatbot:**
   Start the chatbot by running:
   ```bash
   python chatbot.py
   ```

   The bot will start and continuously prompt you for queries. Type `exit` to stop the chatbot.

## Code Structure

- **chatbot.py**: The main script that initializes the LLM, loads data, and handles the user interaction.
- **create_vector_db.py**: This script is responsible for creating the Chroma vector database from PDF documents.
- **requirements.txt**: Lists all dependencies required for the project.
