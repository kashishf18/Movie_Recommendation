# 🎬 Movie Recommendation System

A content-based movie recommender system built with **Python**, **Streamlit**, and the **TMDB API**. Simply select a movie and instantly get 5 similar movie recommendations along with their posters.

---

## 🖥️ Demo

> Select any movie from the dropdown → Click **Show Recommendation** → Get 5 similar movies with posters!

---

## 🚀 Features

- 🔍 **Content-Based Filtering** — Recommends movies based on similarity in genres, cast, crew, keywords, and overview
- 🎞️ **Movie Posters** — Fetches real-time posters via the TMDB API
- ⚡ **Fast & Interactive UI** — Built with Streamlit for a clean, responsive interface
- 📦 **Pre-trained Model** — Uses precomputed cosine similarity for instant recommendations

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Streamlit | Web UI framework |
| Pandas | Data manipulation |
| Scikit-learn | Cosine similarity computation |
| TMDB API | Fetching movie posters |
| Pickle | Model serialization |

---

## 📂 Project Structure

```
Movie_Recommendation/
│
├── app.py                  # Streamlit app — main entry point
├── movie_list.pkl          # Pickled DataFrame of movies
├── movie_dict.pkl          # Pickled movie dictionary
├── similarity.pkl          # Precomputed cosine similarity matrix
├── notebook86c26b4f17.ipynb  # Jupyter notebook for model building & EDA
└── README.md               # Project documentation
```

---

## ⚙️ Setup & Installation

### Prerequisites
- Python 3.8+
- A [TMDB API key](https://www.themoviedb.org/settings/api)

### 1. Clone the repository

```bash
git clone https://github.com/kashishf18/Movie_Recommendation.git
cd Movie_Recommendation
```

### 2. Install dependencies

```bash
pip install streamlit requests pandas scikit-learn
```

### 3. Run the app

```bash
streamlit run app.py
```

---

## 🔑 API Key

This project uses the [TMDB (The Movie Database) API](https://www.themoviedb.org/) to fetch movie posters.

The API key is currently embedded in `app.py`. To use your own:

1. Register at [https://www.themoviedb.org/](https://www.themoviedb.org/)
2. Go to **Settings → API** and generate a key
3. Replace the key in `app.py`:

```python
url = f"https://api.themoviedb.org/3/movie/{movie_id}?api_key=YOUR_API_KEY&language=en-US"
```

---

## 🧠 How It Works

1. **Data**: Built on the [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) from Kaggle
2. **Feature Engineering**: Extracts and combines genres, keywords, cast, crew, and overview into a single "tags" column
3. **Vectorization**: Converts tags to vectors using `CountVectorizer`
4. **Similarity**: Computes **cosine similarity** between all movie vectors
5. **Recommendation**: For a selected movie, finds the top 5 closest movies by similarity score

---

## 📸 Screenshots

> Run the app locally to see it in action!

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 👩‍💻 Author

**Kashish** — [@kashishf18](https://github.com/kashishf18)
