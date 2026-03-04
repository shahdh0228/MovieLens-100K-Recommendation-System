# 🎬 Movie Recommendation System (MovieLens 100K)

## 📌 Project Overview
This project builds a movie recommendation system using the MovieLens 100K dataset.  
The goal is to recommend movies to users based on rating behavior using collaborative filtering and to evaluate the system using Precision@K.


## 🎯 Problem Statement
Build a recommender system that:
1) Creates a user–item rating matrix  
2) Computes similarity scores for recommendations  
3) Recommends top-rated unseen movies for a given user  
4) Evaluates performance using Precision@10  

**Bonus**
- Item-based collaborative filtering  
- Matrix factorization using SVD (TruncatedSVD)


## 📂 Dataset
MovieLens 100K dataset:
- `u.data` → user ratings (userId, movieId, rating, timestamp)
- `u.item` → movie titles and metadata


## ⚙️ Methods Implemented
### ✅ 1) User-based Collaborative Filtering
- Build a user–item matrix from training ratings
- Compute cosine similarity between users
- Recommend unseen movies using weighted neighbor ratings

### ✅ 2) Item-based Collaborative Filtering (Bonus)
- Compute cosine similarity between movies (items)
- Recommend movies similar to those the user rated highly

### ✅ 3) Matrix Factorization (SVD) (Bonus)
- Use TruncatedSVD to learn latent user/movie factors
- Predict missing ratings and recommend top unseen items


## 📊 Evaluation Metric: Precision@10
Precision@10 measures how many recommended movies in the top 10 are actually relevant (rated ≥ 4 in the test set).


## ✅ Results (Precision@10)
- **User-based CF:** 0.2399  
- **Item-based CF:** 0.2297  
- **SVD:** **0.2649** (best)

Evaluated on **924 users**.

**Conclusion:** SVD performed best because it learns hidden preference patterns (latent factors) beyond direct similarity overlap.


## 🛠️ Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn (cosine similarity, TruncatedSVD)
- Matplotlib / Seaborn
- Jupyter Notebook


## 🚀 How to Run
1) Clone repo  
2) Open the notebook in Jupyter  
3) Ensure `u.data` and `u.item` are available (in the same folder as the notebook)  
4) Run cells top-to-bottom  
