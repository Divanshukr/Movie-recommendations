# Movie-recommendations
# Define a dictionary of movies with genres
movies = {
    "The Shawshank Redemption": "Drama",
    "The Godfather": "Crime",
    "The Dark Knight": "Action",
    "Schindler's List": "Biography",
    "Pulp Fiction": "Crime",
    "The Lord of the Rings: The Return of the King": "Fantasy",
    "Forrest Gump": "Drama",
    "The Matrix": "Action",
    "Titanic": "Romance",
    "Goodfellas": "Crime"
}

# Function to recommend movies based on user input
def recommend_movie(genre):
    recommended_movies = []
    for movie, movie_genre in movies.items():
        if movie_genre.lower() == genre.lower():
            recommended_movies.append(movie)
    return recommended_movies

# Main function
def main():
    print("Welcome to Movie Recommender!")
    user_genre = input("Enter your preferred genre: ")
    recommended_movies = recommend_movie(user_genre)
    if recommended_movies:
        print("Here are some recommended movies for the genre", user_genre + ":")
        for movie in recommended_movies:
            print("-", movie)
    else:
        print("Sorry, no movies found for the genre", user_genre)

if __name__ == "__main__":
    main()
