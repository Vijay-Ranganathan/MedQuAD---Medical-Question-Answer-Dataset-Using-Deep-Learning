# MedQuAD Chatbot

A chatbot leveraging the MedQuAD dataset and NLP to provide answers to medical questions. It uses Sentence Transformers for generating embeddings and cosine similarity for matching user queries with the dataset.

## Features
- Uses `SentenceTransformer` model for semantic understanding.
- Matches user queries with questions from the MedQuAD dataset.
- Provides accurate answers based on the closest match.

## Prerequisites
- Python 3.7 or later
- `medquad.csv` file containing the MedQuAD dataset

## Installation
1. Clone the repository and navigate to the project directory.
2. Install the required Python packages:
    ```bash
    pip install scikit-learn pandas sentence-transformers
    ```

## Usage
1. Place the `medquad.csv` file in the project directory.
2. Run the script:
    ```bash
    python chatbot.py
    ```
3. Interact with the chatbot by typing your medical questions.

## File Description
- `medquad.csv`: The dataset containing medical questions and answers.
- `chatbot.py`: The main script implementing the chatbot functionality.

## How It Works
1. **Load Dataset**: The MedQuAD dataset is loaded into a Pandas DataFrame.
2. **Generate Embeddings**: Each question in the dataset is converted into a numerical representation using the `SentenceTransformer` model.
3. **Query Matching**: User queries are embedded and matched with dataset questions using cosine similarity.
4. **Response Generation**: The chatbot returns the answer corresponding to the most similar question.

## Example Interaction
```text
Welcome to the MedQuAD Chatbot! Ask a medical question, or type 'exit' to quit.
You: What are the symptoms of diabetes?
Chatbot: Frequent urination, increased thirst, and unexplained weight loss. (Matched Question: What are the symptoms of diabetes?)
You: exit
Chatbot: Goodbye!
