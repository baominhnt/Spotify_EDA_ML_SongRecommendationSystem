# Spotify_EDA_ML_SongRecommendationSystem
🎵 Spotify Song Recommendation System
A Hybrid Machine Learning Recommender using Audio Features, Genre Preferences, and XGBoost

📌 Overview
This project builds a hybrid song recommendation system using the Spotify Tracks Dataset.
It combines:

- Content-based similarity (cosine similarity on scaled audio features)
- Genre preference matching
- Hit probability prediction using XGBoost

The result is a personalized recommender that suggests songs similar to a user‑selected track while also considering genre preferences and popularity likelihood.

The notebook also includes EDA, feature engineering, and machine learning modeling to understand what makes a song popular.

🚀 Features
🎧 Hybrid Recommendation Engine
The system blends three components:

Component	          Description	                                        Weight
Similarity Score	  Cosine similarity between scaled audio features	    0.5
Hit Probability	      XGBoost classifier predicting if a track is a “hit”	0.3
Genre Match	          Whether the track matches user-selected genres	    0.2
This hybrid scoring method produces recommendations that are:
- Sonically similar
- Aligned with user taste
- Likely to be popular

📊 Exploratory Data Analysis (EDA)
The notebook includes:
- Feature distributions
- Popularity trends
- Genre-level insights
- Correlation heatmaps
- Interaction feature exploration

🧠 Machine Learning
The project trains an XGBoost classifier to predict whether a song is a “hit” (top 10% popularity).
Key steps include:
- Train/test split
- Standard scaling
- Cyclical encoding for musical key
- Interaction features
- Model evaluation

🔍 Track Name Search
Users can input any track name, and the system will:
- Find the exact match
- Fall back to partial matching if needed
- Compute similarity on the fly (memory‑safe)

📦 Clean Output
The recommender returns a compact DataFrame containing:
- track_name
- artists
- album_name
- track_genre
Perfect for display or UI integration.

🛠️ Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib, Seaborn
- Cosine Similarity
- Google Colab

📁 Project Structure

Spotify_Song_Recommendation_System.ipynb
data/
    spotify-tracks-dataset.csv
README.md
▶️ Example Usage
python
track_name = "Comedy"
user_genres = ["acoustic", "pop"] recommend_hybrid_by_name(track_name, user_genres).

Example output:

``` text
        track_name              artists               album_name        track_genre
0          Comedy           Gen Hoshino                 Comedy           acoustic
1         JAMAICA            Feid;Sech   Halloween 2022 Vol. 4               pop
2     Have It All           Jason Mraz            Have It All           acoustic
...
```
🧩 How It Works
1. User enters a track name
2. System finds the track index (exact or partial match)
3. Computes cosine similarity with all tracks
4. Computes genre match
5. Predicts hit probability using XGBoost
6. Combines all three into a hybrid score
7. Returns the top N recommended songs

🔮 Future Improvements
- Mood-based filtering (energy, valence, tempo)
- Artist similarity modeling
- Collaborative filtering
- Streamlit web app
- Album cover images via Spotify API

🙌 Acknowledgements
Dataset: Spotify Tracks Dataset (Kaggle)  
This project was created to explore music analytics, machine learning, and recommender system design.

📬 Contact 

For questions, collaboration, or feedback: James Nguyen
Data Analyst & Dashboard Designer (Linkedin: https://www.linkedin.com/in/tran-bao-minh-nguyen-296b01333/
For more projects finding:https://baominhnt.github.io/tbmnguyen.com/index.html)
