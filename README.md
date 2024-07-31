# Simple Movie Recommender

This project demonstrates how to use a vector database to recommend movies based on user ratings. By leveraging matrix factorization and vector search, we can create personalized movie recommendations. The dataset used is the [MovieLens Latest Small Dataset](https://grouplens.org/datasets/movielens/latest/), which contains 100,000 ratings and 3,600 tags applied to 9,000 movies by 600 users.

## Overview

The approach taken involves:
1. Loading the MovieLens dataset and preparing it for analysis.
2. Computing ratings and constructing a review matrix.
3. Using matrix factorization to derive content embeddings.
4. Creating a vector database with relevant movie metadata.
5. Generating movie recommendations based on content similarity.

## Dataset

The dataset used is the MovieLens Latest Small Dataset, which includes:
- `ratings.csv`: User ratings for different movies.
- `movies.csv`: Metadata about the movies.
- `links.csv`: Additional links, such as IMDb IDs for movies.

## Methodology

1. **Loading Data:** The dataset is loaded and processed, starting with `ratings.csv` to compute content embeddings.
2. **Computing Ratings:** A pivot table is created from the ratings data, representing user-movie interactions.
3. **Computing Embeddings:** Matrix factorization using SVD is applied to extract content embeddings from the review matrix.
4. **Metadata Alignment:** The movies metadata is aligned with the embeddings dataframe.
5. **Vector Database Creation:** A table is created with fields for movie ID, embeddings, genres, title, and IMDb ID.
6. **Generating Recommendations:** Recommendations are generated based on the similarity of content vectors.

## Installation

To set up the project, clone the repository and install the required packages using the following command:

```bash
pip install -r requirements.txt
