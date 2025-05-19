# 📚 Book Recommendation System

This is a simple content-based and collaborative filtering book recommendation system built using the [Book-Crossings dataset](https://www.kaggle.com/datasets/ruchi798/bookcrossing-dataset). The goal is to recommend books that are similar to a given title based on user ratings.

## 🔍 Overview

The system:
- Loads and cleans user ratings and book metadata
- Filters active users and popular books
- Builds a pivot matrix of user ratings per book
- Applies **k-nearest neighbors (KNN)** with **cosine similarity** to recommend similar books

## 🛠️ Technologies Used

- Python 🐍
- Pandas & NumPy for data manipulation
- Scikit-learn for machine learning
- SciPy for sparse matrix operations
- Matplotlib for visualization (optional)
- Google Colab (for development)

## 📁 Dataset

The dataset used is the Book-Crossing dataset, consisting of:
- `BX-Books.csv` — metadata about books
- `BX-Book-Ratings.csv` — user ratings for books

Download:  
```bash
wget https://cdn.freecodecamp.org/project-data/books/book-crossings.zip
unzip book-crossings.zip
🚀 How It Works
Load Data: Read in book and rating data from CSVs.

Filter: Keep users with ≥ 200 ratings and books with ≥ 100 ratings.

Pivot: Convert data to a book-user matrix (books as rows, users as columns).

Train Model: Fit a KNN model using cosine similarity on the sparse matrix.

Recommend: Given a book title, return 5 most similar books.

🧪 Sample Usage
get_recommends('The Catcher in the Rye')
Example Output:
['The Catcher in the Rye',
 [['Tis: A Memoir', 0.78],
  ["ANGELA'S ASHES", 0.77],
  ['Their Eyes Were Watching God: A Novel', 0.77],
  ['1984', 0.76],
  ['To Kill a Mockingbird', 0.76]]]
✅ Test Function
A test case is included to verify if the system recommends the expected titles:
test_book_recommendation()
Output if passed:
ed the challenge! 🎉🎉🎉🎉🎉
📌 Notes
Sparse matrices are used to improve performance and memory usage.

Only highly rated books and active users are included for better accuracy.

The system does not require deep learning — it's pure scikit-learn.

📎 License
This project is for educational purposes and uses open datasets.

🧠 Inspired by:
FreeCodeCamp Data Science Projects

Book-Crossings dataset

