# 🎬 Movie Recommender System 🍿

This project is a **Movie Recommendation System** built with **Streamlit** that suggests movies based on a similarity score. The recommendations are made using cosine similarity on movie data, and posters of the recommended movies are displayed using **The Movie Database (TMDb) API**.

# Dataset : https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

## 🛠️ Features

- Recommend **5 similar movies** based on the movie you select.
- Display the **poster** of each recommended movie.
- Easy-to-use **Streamlit** interface for selecting a movie and viewing recommendations.
- **Deployed on Heroku** for easy access.

---

## 🚀 How to Run Locally?

### 1. Clone the repository

```bash
git clone https://github.com/your-username/movie-recommender-system.git
cd movie-recommender-system
```

2. Create a virtual environment and activate it
```python
# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate   # On Windows use `venv\Scripts\activate`
```
3. Install Dependencies
```python
pip install -r requirements.txt
```
4. Run the application
```python
streamlit run app.py
```

#🖥️ Heroku Deployment
The Movie Recommender System is deployed on Heroku. Follow the steps below to deploy the project on Heroku:

1. Create a Heroku account
Go to Heroku and sign up for a free account.

2. Install the Heroku CLI
If you don't already have it installed, follow the instructions on Heroku CLI Installation to install it.

3. Log in to Heroku from your CLI

4. Create a new Heroku app
   ```bash
   heroku create movie-recommender-app
   ```
5. Push your code to Heroku
   ```bash
   git add .
   git commit -m "Initial commit"
   git push heroku master
   ```
6. Scale the app to run one web instance
```bash
heroku ps:scale web=1
```
8. Open your deployed app
```bash
heroku open
```
#🔧 API and Data
TMDb API
The application uses the TMDb API to fetch movie posters. You can get your own API key by signing up on The Movie Database.

The API key is stored in the code as:
```python
url = "https://api.themoviedb.org/3/movie/{}?api_key=YOUR_API_KEY&language=en-US"
```
# 👩‍💻 How the App Works
Movie Selection: Users can select a movie from the dropdown list, which contains titles of movies from the dataset.
Recommendation: Once a movie is selected and the "Show Recommendation" button is clicked, the app fetches 5 similar movies using a precomputed similarity matrix.
Display: The titles and posters of the recommended movies are displayed in a row.

#🔮 Future Improvements
Add more data and enhance the recommendation system to use collaborative filtering.
Improve the user interface with additional features such as search and filters.
Add functionality for movie trailers and more detailed movie information.


