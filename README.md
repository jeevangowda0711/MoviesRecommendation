# Movie Recommendation System

## Overview

The **Movie Recommendation System** is a Python-based web application developed using **Streamlit** to recommend movies based on user input. The project uses **TMDB (The Movie Database) API** to fetch movie posters and **Cosine Similarity** to suggest movies that are similar to a selected title. The recommendation system processes a dataset containing over **5,000 movies** and provides users with five movie suggestions along with their posters.

## Features

- **Movie Recommendation**: Recommends 5 similar movies based on the selected movie title using a **content-based filtering** approach.
- **Poster Fetching**: Automatically fetches movie posters from the **TMDB API** to enhance user experience.
- **Interactive Web Interface**: Built with **Streamlit**, offering an easy-to-use and interactive interface for users to select movies and view recommendations.
  
## Technology Stack

### Libraries and Tools
- **Python**: Core programming language for the application.
- **Streamlit**: For building the interactive web-based interface.
- **TMDB API**: For fetching movie posters based on movie IDs.
- **Pandas**: Data processing and manipulation.
- **Sklearn (Scikit-learn)**: For implementing **Cosine Similarity** and text vectorization.
- **Pickle**: For saving the movie list and similarity matrix for quick future access.

### Dataset
The dataset used consists of over **5,000 movies** with the following fields:

```plaintext
budget,genres,homepage,id,keywords,original_language,original_title,overview,popularity,production_companies,production_countries,release_date,revenue,runtime,spoken_languages,status,tagline,title,vote_average,vote_count
```

**Example Data:**
```plaintext
237000000,"[{""id"": 28, ""name"": ""Action""}, {""id"": 12, ""name"": ""Adventure""}, {""id"": 14, ""name"": ""Fantasy""}, {""id"": 878, ""name"": ""Science Fiction""}]",http://www.avatarmovie.com/,19995,"[{""id"": 1463, ""name"": ""culture clash""}, {""id"": 2964, ""name"": ""future""}]",en,Avatar,"In the 22nd century, a paraplegic Marine is dispatched to the moon Pandora on a unique mission.",150.437577,"[{""name"": ""Ingenious Film Partners"", ""id"": 289}]",2009-12-10,2787965087,162,"[{""iso_639_1"": ""en"", ""name"": ""English""}]"
```

### Setup Instructions

### Prerequisites

Before setting up the project, ensure you have the following installed:

- **Python 3.x**
- **Pip** (Python package installer)

### Installation Steps

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/jeevangowda0711/MoviesRecommendation.git
   cd MoviesRecommendation
   ```

2. **Create and Activate a Virtual Environment:**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install the Required Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application:**

   ```bash
   streamlit run app.py
   ```

   This will launch the web application on your local server. Open your browser and go to the provided URL (usually `http://localhost:8501/`).

## Usage

1. **Select a Movie**: Use the dropdown menu to select a movie from the list of available titles.
2. **Show Recommendations**: Click the "Show Recommendation" button to view 5 recommended movies along with their posters.
3. **View Results**: The recommendations will be displayed in a grid, showing the movie titles and posters fetched from the **TMDB API**.

## How the Recommendation Works

- **Content-Based Filtering**: The system uses **Count Vectorization** to convert movie metadata (title, genres, cast, crew, keywords) into vectors.
- **Cosine Similarity**: The cosine similarity of these vectors is then computed to identify movies that are most similar to the selected title.
- **Recommendations**: The system suggests the top 5 movies that are most similar to the user's selection based on the calculated similarity.

## Example Movies in Dataset

- **Avatar**
- **Pirates of the Caribbean: At World's End**
- **The Dark Knight Rises**
- **John Carter**
- **Spectre**

## Project Files

- **app.py**: Main file containing the Streamlit app code and recommendation logic.
- **notebook.ipynb**: Jupyter notebook used for data preprocessing and model training.
- **movie_list.pkl**: Pickled file containing the list of movies.
- **similarity.pkl**: Pickled file containing the precomputed similarity matrix.
- **tmdb_5000_movies.csv**: Movie dataset used for recommendations.
- **requirements.txt**: List of required Python packages for running the project.

## Future Enhancements

- Improve recommendation accuracy by incorporating user ratings and reviews into the model.
- Add more advanced filtering options such as genre-based recommendations.
- Integrate a more robust dataset with a larger number of movies.

## License

This project is licensed under the MIT License.

---

## Acknowledgments

- **TMDB API** for providing access to movie metadata and posters.
- **Streamlit** for providing an easy-to-use framework for building web applications.
- **Scikit-learn** for offering a comprehensive set of machine learning tools used for similarity calculations.
