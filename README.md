# Movie-Recommendation-System

This project is a movie recommendation system built using Natural Language Processing (NLP) techniques. The system recommends movies based on their genre similarity using TF-IDF and Cosine Similarity.

## Overview

This project leverages a movie dataset to build a content-based recommendation engine. It uses genres of the movies to compute the similarity between different movies and recommends similar movies to the user.

## Dataset

- The movie dataset is sourced from an external CSV file and contains information such as:
  - Movie title
  - Genres
  - Budget
  - Additional metadata

For more details about the dataset contact the author. (rsivaakash@gmail.com)

## Key Features

- **Content-based Filtering**: Recommendations are generated based on the genres of the movies.
- **TF-IDF Vectorization**: Text data (movie genres) is converted into a matrix of TF-IDF features.
- **Cosine Similarity**: The cosine similarity metric is used to find movies that are similar to the one chosen by the user.

## Libraries Used

- `numpy`: For numerical computations.
- `pandas`: For data manipulation and analysis.
- `scikit-learn`:
  - `TfidfVectorizer`: To convert text data into TF-IDF vectors.
  - `cosine_similarity`: To calculate similarity between movies based on their genres.
- `difflib`: For finding close matches to movie titles.

## Instructions for Running the Project

1. **Mount Google Drive**: Ensure that the dataset is loaded from Google Drive.
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```

2. **Download the Dataset**: The dataset is fetched from Google Drive using the `gdown` tool.
    ```bash
    ! gdown --id <file_id>
    ```

3. **Install Necessary Libraries**: Ensure that all dependencies are installed.
    ```bash
    pip install numpy pandas scikit-learn
    ```

4. **Run the Notebook**: Execute the notebook cells in order to preprocess the data, compute TF-IDF vectors, and generate movie recommendations.

## How It Works

1. The dataset is loaded, and movie genres are extracted.
2. TF-IDF vectorization is applied to convert the genre text into vectors.
3. Cosine similarity is computed between the vectors.
4. Based on the similarity scores, movies that are closest to the user's selected movie are recommended.

## Example

If the user selects the movie `Inception`, the system will recommend movies with similar genres, such as `Interstellar` or `The Matrix`.

## Authors

- **Siva Akash Ramini**

## Acknowledgments

- This project was developed as part of an NLP and recommendation systems study.