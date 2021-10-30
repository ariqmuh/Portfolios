# Analyze Movie Features Correlation to Gross

## 🔸 Dataset Source: 
[Kaggle](https://www.kaggle.com/danielgrijalvas/movies)

## 🔸 Objective: 
Find the correlated features to gross or revenue of the movie

## 🔸 Content:
There are 6820 movies in the dataset (220 movies per year, 1986-2016). Each movie has the following attributes:
- budget: the budget of a movie. Some movies don't have this, so it appears as 0
- company: the production company
- country: country of origin
- director: the director
- genre: main genre of the movie.
- gross: revenue of the movie
- name: name of the movie
- rating: rating of the movie (R, PG, etc.)
- released: release date (YYYY-MM-DD)
- runtime: duration of the movie
- score: IMDb user rating
- votes: number of user votes
- star: main actor/actress
- writer: writer of the movie
- year: year of release

## 🔸 Result:
<p align="center">
  <img src="https://user-images.githubusercontent.com/82768391/139525564-3fb0631e-6fd6-483a-99a1-3501fee3d979.png" />
</p>

From the heatmap above, we can conclude that Votes and Budget variables have the strong positive correlation to Gross variables.
- Budget = 0.74
- Votes = 0.64
