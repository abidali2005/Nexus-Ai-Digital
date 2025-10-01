# 🎬 Movie Recommendation System (Content-Based)

## 📌 Project Overview
GlobalMart wants to boost sales by suggesting products users are likely to buy, similar to how Amazon and Netflix recommend content.  
In this project, we build a **Content-Based Movie Recommendation System** using the **TMDB 5000 Movie Dataset** from Kaggle.  

The system suggests movies to a user based on the content (genres, cast, crew, keywords, overview) of movies they have previously liked.

---

## 📂 Dataset Description
We are provided with two files:

1. **tmdb_5000_credits.csv**  
   - Columns:  
     - `movie_id` → Unique ID for the movie  
     - `title` → Movie name  
     - `cast` → Main actors in the movie  
     - `crew` → Crew details (directors, producers, etc.)  

2. **tmdb_5000_movies.csv**  
   - Columns:  
     - `id` → Movie ID (links with `movie_id` from credits file)  
     - `title` → Movie name  
     - `genres` → Genre(s) of the movie  
     - `keywords` → Keywords related to the movie  
     - `overview` → Short description of the movie  
     - Other metadata like budget, revenue, release_date, vote_count, etc.  

---

## 🔗 Data Merging
- The two files are merged together using the **common key**:  
  - `movies.id` ↔ `credits.movie_id`  
- After merging, we get a **single dataframe** containing both content details and credits.

---

## 🧹 Data Preprocessing
Steps performed before building the recommender:
1. **Selecting useful columns**:  
   We only need `movie_id`, `title`, `overview`, `genres`, `keywords`, `cast`, and `crew`.
2. **Handling Missing Values**:  
   Remove or fill missing values in `overview`, `genres`, or other important fields.
3. **Data Cleaning**:  
   - Convert JSON-like strings (`genres`, `keywords`, `cast`, `crew`) into lists of words.  
   - Extract important crew members (e.g., Director).  
   - Keep only top 3 actors from the cast to avoid noise.  
   - Remove spaces in multi-word tokens (e.g., "Science Fiction" → "ScienceFiction").  
4. **Creating Tags Column**:  
   Combine all important text features (`overview + genres + keywords + cast + crew`) into a single column called **`tags`**.  
   This `tags` column represents the movie content in textual form.

---

## 📊 Feature Extraction
- Use **TF-IDF Vectorizer** or **Count Vectorizer** to convert the `tags` column into a numerical matrix.  
- Each movie is represented as a vector of numbers, based on word frequency and importance.

---

## 📐 Similarity Calculation
- Use **Cosine Similarity** to compute the similarity between movies.  
- This gives us a similarity score between every pair of movies.  
- Movies with higher scores are considered more similar.

---

## 🛠️ Recommender System
- Build a function `recommend(movie_title)` that:  
  1. Finds the index of the given movie in the dataset.  
  2. Looks at the similarity scores for that movie.  
  3. Sorts the movies by similarity score.  
  4. Returns the **Top 5 most similar movies**.

---

## 📌 Example Usage
If the user likes **"Avatar"**, the system might recommend:
- Guardians of the Galaxy  
- Star Trek  
- Star Wars  
- The Fifth Element  
- Interstellar  

---

## ✅ Key Takeaways
- We combined two datasets (`movies` + `credits`) using movie IDs.  
- Created a single `tags` column containing overview, genres, keywords, cast, and crew.  
- Used **TF-IDF/Count Vectorizer** for feature extraction.  
- Applied **Cosine Similarity** to find related movies.  
- Built a simple recommender function to suggest top similar movies.  

---

## 🚀 Future Enhancements
- Improve recommendations using **hybrid models** (Content + Collaborative Filtering).  
- Include user ratings and popularity in recommendation logic.  
- Deploy the system using **Flask / Streamlit** with an interactive UI.
