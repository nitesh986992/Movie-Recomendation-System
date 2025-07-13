Movie Recommendation System
Overview
This project presents a content-based movie recommendation system using data from the TMDB 5000 dataset. The objective is to suggest movies similar to a given input title by analyzing metadata such as cast, crew, genres, and keywords.

Dataset
The project uses two datasets:

tmdb_5000_movies.csv

tmdb_5000_credits.csv

These datasets were merged on the title field to form a unified dataset containing the following relevant columns:

movie_id

title

overview

genres

keywords

cast

crew

Key Steps
Data Loading
The datasets are loaded using Pandas and merged on the movie title.

Data Cleaning

Missing values are handled by dropping rows with null entries.

Irrelevant columns are removed, retaining only those necessary for the recommendation logic.

Feature Engineering
The following steps are typically included (assumed based on standard practice, to be confirmed from later notebook cells):

Extraction of genre names, actor names, and crew details.

Construction of a textual "tags" field combining all relevant information.

Vectorization using TF-IDF or CountVectorizer.

Similarity calculation using cosine similarity.

Recommendation Logic
Given a movie title, the system returns the top N similar movies based on cosine similarity scores of the feature vectors.

Requirements
Python 3.x

Pandas

NumPy

scikit-learn


pip install pandas numpy scikit-learn


How to Run
Ensure the required CSV files are in the working directory.

Run the Jupyter Notebook 1d1e20e4-638d-484b-8856-28c9672775a7.ipynb.

Use the final recommendation function by passing a movie title to get suggestions.

Future Improvements
Include a web interface using Streamlit or Flask.

Add collaborative filtering-based recommendations.

Integrate more metadata such as user ratings or release year.
