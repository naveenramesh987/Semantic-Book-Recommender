# Semantic Book Recommender

A book recommendation system that uses semantic search and sentiment analysis to find books based on natural language descriptions and emotional tones.

## 📖 Overview

This project goes beyond simple keyword matching by leveraging **semantic vector search**. It allows users to describe the *kind* of book they want to read (e.g., "a story about forgiveness" or "a book to teach children about nature") and filters the results based on emotional categories (Happy, Surprising, Angry, Suspenseful, Sad).

The system is built using **LangChain**, **ChromaDB**, and **Hugging Face** embeddings, with a user-friendly web interface powered by **Gradio**.

## ✨ Key Features

* **Semantic Search Engine**: Uses `all-MiniLM-L6-v2` embeddings to understand the context and meaning of user queries.
* **Emotion-Based Filtering**: Sorts recommendations by emotional tone derived from sentiment analysis.
* **Category Filtering**: Allows users to narrow down results by specific book categories (Fiction, Nonfiction, etc.).
* **Interactive Dashboard**: A clean, browser-based UI using Gradio to display book covers and descriptions.

## 🛠️ Tech Stack

* **Python**: Core programming language.
* **Gradio**: Web dashboard interface.
* **LangChain**: Framework for LLM and vector store integration.
* **ChromaDB**: Vector database for storing and retrieving book embeddings.
* **Hugging Face**: Source for the sentence transformer models.
* **Pandas & NumPy**: Data manipulation and analysis.

## 🚀 Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/naveenramesh987/semantic-book-recommender.git](https://github.com/naveenramesh987/semantic-book-recommender.git)
    cd semantic-book-recommender
    ```

2.  **Install the required dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install pandas numpy gradio python-dotenv langchain-community langchain-huggingface langchain-chroma scikit-learn matplotlib seaborn
    ```

3.  **Environment Setup:**
    Create a `.env` file in the root directory if you need to store API keys (though the current model `all-MiniLM-L6-v2` runs locally without an API key).

## 📊 Data Preparation

The project includes several Jupyter notebooks that handle data processing:

1.  **`data-exploration.ipynb`**: Initial exploration and cleaning of the dataset.
2.  **`sentiment-analysis.ipynb`**: Analyzes book descriptions to assign emotional scores (Joy, Anger, Surprise, etc.) and generates `books_with_emotions.csv`.
3.  **`vector-search.ipynb`**: Generates the vector embeddings and creates `tagged_description.txt` used by the semantic search engine.

*Note: Ensure `books_with_emotions.csv` and `tagged_description.txt` are present in the root directory before running the app.*

## 🖥️ Usage

To launch the recommendation dashboard:

```bash
python gradio-dashboard.py
