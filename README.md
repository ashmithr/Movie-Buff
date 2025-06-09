# 🎬 Content-Based Movie Recommendation System

A content-based movie recommender built using **TF-IDF** (Term Frequency-Inverse Document Frequency) and **cosine similarity** on movie content. This system is designed to provide fast, interactive movie suggestions based on the characteristics of movies you enjoy.

---

## ✨ Features

* **Content-Based Filtering:** Recommends movies similar to your chosen movie based on their genres, keywords, cast, and crew.
* **TF-IDF Vectorization:** Transforms movie text data into numerical representations, capturing the importance of words.
* **Cosine Similarity:** Measures the similarity between movie vectors to find the most relevant recommendations.
* **Interactive User Interface:** Built with **Streamlit** for a user-friendly and engaging experience.
* **Fast Recommendations:** Designed for quick processing and immediate movie suggestions.

---

## 🚀 Technologies Used

* **Python:** The core programming language for the recommendation logic.
* **Streamlit:** For creating the interactive web application.
* **scikit-learn:** For TF-IDF vectorization and cosine similarity calculations.
* **Pandas:** For data manipulation and analysis.

---

## ⚙️ Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/movie-recommendation-system.git](https://github.com/YourUsername/movie-recommendation-system.git)
    cd movie-recommendation-system
    ```
    (Replace `YourUsername` with your actual GitHub username or the repository's owner.)

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

---

## 🏃 How to Run

1.  **Configure your OMDb API Key:**
    Before running, open `config.json` and replace `"YOUR_OMDB_API_KEY"` with your actual OMDb API key.

2.  **Navigate to the `src` directory:**
    ```bash
    cd src
    ```

3.  **Run the preprocessing script:** This script will likely prepare your movie data for the recommendation system.
    ```bash
    python preprocess.py
    ```

4.  **Launch the Streamlit application:**
    ```bash
    streamlit run main.py
    ```

5.  The application will open in your web browser, typically at `http://localhost:8501`.

---

## 💡 How it Works

The system processes movie metadata (e.g., plot summaries, genres, cast, crew) to create a "content profile" for each movie.

1.  **Data Preprocessing:** Raw movie data is cleaned and combined into a single string for each movie.
2.  **TF-IDF Vectorization:** The combined text for all movies is transformed into TF-IDF vectors. This numerical representation highlights words that are important and relevant to a specific movie within the entire dataset.
3.  **Cosine Similarity Calculation:** When you select a movie, its TF-IDF vector is compared to all other movie vectors using cosine similarity. Cosine similarity measures the angle between two vectors, with a smaller angle indicating higher similarity.
4.  **Recommendation Generation:** The movies with the highest cosine similarity scores to your selected movie are presented as recommendations.
