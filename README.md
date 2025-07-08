# 🎬 Movie Recommendation System

This is a **content-based movie recommendation system** that suggests movies using cast and director information from the TMDB 5000 Movie Credits dataset. It also includes **data visualizations** like top actors, most recommended movies, and clustering of movie tags.

---

## 📌 Features

- ✅ Recommend top 5 movies similar to a given title (based on cast + director)
- 🎭 Visualize the top 10 most frequent actors
- 📊 See the most and least recommended movies
- 🧠 Clustering of movies using **KMeans** and **SVD** for dimensionality reduction
- 📈 Bar charts for quick insights into recommendations and trends

---

## 📁 Dataset

This project uses:

- `tmdb_5000_credits.csv`  
  📌 Download from [Kaggle - TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

Place the CSV file in the same directory as your script.

---

## ⚙️ How It Works

### 1. **Preprocessing**
- Extracts top 3 cast members and director names
- Combines them into a `tags` field for vectorization

### 2. **Vectorization & Similarity**
- Applies `CountVectorizer` to the tags
- Computes **cosine similarity** between all movies
- Recommends top K similar titles for a given movie

### 3. **Visualizations**
- Bar chart of **top 10 actors**
- Recommendations plotted for any movie title (e.g., "Avatar")
- Most and least frequently recommended movies shown graphically

### 4. **Clustering (Optional Advanced)**
- Reduces feature vectors using **TruncatedSVD**
- Applies **KMeans clustering** to group movies by feature similarity

---

## 📷 Example Outputs

### 🔎 Top 5 Similar Movies to `Avatar`
![avatar-recommendations]![Screenshot (48)](https://github.com/user-attachments/assets/e28d6b95-14b1-4a5a-b597-13027eacafbf)

### 🌟 Top 10 Most Recommended Movies
![most-recommended]![Screenshot 2025-06-16 164358](https://github.com/user-attachments/assets/b9f4781f-7884-4f10-949d-4f6620c46075)

### 📉 Least Recommended Movies
![least-recommended]![o0](https://github.com/user-attachments/assets/4820a458-2e96-472b-812e-5d314a345ca2)

> *(You can generate these by running the script — make sure `matplotlib` is installed)*

---

## 🛠️ Requirements

Install dependencies using pip:

```bash
pip install pandas matplotlib scikit-learn

