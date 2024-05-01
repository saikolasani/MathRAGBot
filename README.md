# MathRAGBot - Chat Agent that uses RAG to solve Math Word Problems

This repository contains the implementation of a Retrieval-Augmented Generation (RAG) model using AstraDB and OpenAI's embeddings. It is designed to demonstrate how you can leverage AstraDB's vector storage capabilities to perform similarity searches on a dataset of documents, using embeddings generated by OpenAI models.

## Features

- Uses OpenAI's embedding models for generating vector representations of documents.
- Stores and retrieves documents using AstraDB's vector storage capabilities.
- Includes a sample retrieval of documents based on similarity search.

## Requirements

Before running this code, ensure you have the following installed:
- Python 3.7+
- `langchain_astradb`
- `transformers`
- `langchain_openai`
- `langchain_core`
- `datasets`

You can install the required packages using pip:

```bash
pip install langchain_astradb transformers langchain_openai langchain_core datasets
```

## Dataset

The code uses the `microsoft/orca-math-word-problems-200k` dataset from the Hugging Face `datasets` library. This dataset contains over 200,000 math word problems. The script can be modified to use any dataset by replacing the dataset identifier with a new dataset available in the Hugging Face library.

Example change to use a different dataset:

```python
# Replace the line below with the identifier of new dataset
dataset = load_dataset("new_dataset_identifier", split='train')
```

## Interactive Chat 

The code integrates LLaMA 2 Chatbot to provide an interactive chat feature, which allows users to ask and receive answers to math problems interactively. Below is an example of an interactive chat session where the user asks a variety of questions related to math problems, demonstrating the capability of the system to understand and respond accurately.

### Chat Session Example

```plaintext
LLaMA 2 Chatbot: I'm here to help with math problems. Ask me anything!
You: Jungkook is the 5th place. Find the number of people who crossed the finish line faster than Jungkook.
LLaMA 2 Chatbot: Sure! Here is the answer to the user question:
4 people

You: The length of one span of Jinseo is about 10 centimeters (cm). When Jinseo measured the length of the shorter side of the
LLaMA 2 Chatbot: Sure! Here is the answer to the user question:
2 spans * 10 cm/span = 20 cm

You: What is the difference between the largest number and the smallest number that can be made by selecting four from the numk
LLaMA 2 Chatbot: The difference between the largest and smallest four-digit numbers that can be made by selecting four from t
```

### Running the Interactive Chat in the Notebook

To engage with the interactive chat feature powered by the LLaMA 2 Chatbot, a session can be initiated by running the `interactive_chat()` function provided in the code. This function activates the chatbot, which can then respond to your queries, particularly useful for solving math problems or exploring dataset content interactively.

### How to Run the Interactive Chat Locally

Follow these steps to start the interactive chat:

1. Ensure all dependencies are installed and your environment variables are set (as described in the #Requirements section).
2. Open the terminal or command prompt where your script is located.
3. Execute the script using Python. For example:
   ```bash
   python astradbrag.py

