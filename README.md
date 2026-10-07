# DSA4060 Personalised Movie Recommender
## Amy Njenga - 668698 (userId = 19)


## Objectives
The following project aims to create a simple movie recommendation system using content-based filtering. The process involves the creation of a user-item matrix which links a single user to the movies the rated, the movie ratings, the movie genre etc. This then helps us create a user preference profile which then informs our recommendation score which is then used to create a ranked list of personalised recommendations.

## Dataset Description
The project makes use of two datasets. The "movies" csv and the "ratings" csv. The "movies" csv contains columns showing the movieId, title and genre. The "ratings" csv contains columns indicating userId, movieId, rating and the timestamp; so basically user interactions.

## Approach
The projected aimed to determine a user's preference using specific item features. 

In our case, the features are the movie genres. 
The process of identifying the preference would be: 
1. Identify the movies rated most highly by the user
2. Identify the genres of those movie
3. Encode the features using one-hot encoding
4. Create a user profile by summing the feature vectors
5. Turn the features into proportions that help us better understand their contribution to the preference profile
6. Calculate the similarity between the normalised genre vector and the genre vector using the dot product.
7. Using the similarity score as the recommendation score



## How to run
1. Clone the repository
2. Install packages
3. Place the required CSV files in `data/` if they are omitted 
4. Open `dsa4060_668698.ipynb`
5. Run all cells from top to bottom


## Results
The result is a ranked list of the movies with the highest recommendation score, These include but are not limited to: 
Rubber (2010)
Interstate 60 (2002)
Aqua Teen Hunger Force Colon Movie 
Maximum Ride (2016)
Dragonheart 2: A New Beginning (2000)



## Limitation and improvement

The limitation of the method is the reliance on surface level similarities between items. In our case, the feature considered are movie genres, but that may not adequately capture why a user rated that movie highly.

A possible mitigation strategy would be the use of the film's metadata in the creation of the features
