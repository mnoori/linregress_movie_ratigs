#Linear regression with movie ratings dataset
** Table of Contents
** [Introduction](#intro)
** [Structure of dataset](#struct)
** [Goal of Analysis](#goal)

## <a name="intro"></a>Introduction
The dataset contains information on how major movie review services rated movies. The data originally came from [FiveThirtyEight](https://fivethirtyeight.com/features/fandango-movies-ratings/). Each row represents a single movie. Each column contains information about how the online moview review services RottenTomatoes, Metacritic, IMDB, and Fandango rated the movie. The dataset was put together to help detect bias in the movie review sites. Each of these sites has 2 types of score -- User scores, which aggregate user reviews, and Critic score, which aggregate professional critical reviews of the movie. Each service puts their ratings on a different scale:

* RottenTomatoes - 0-100, in increments of 1.
* Metacritic - 0-100, in increments of 1.
* IMDB - 0-10, in increments of .1.
* Fandango - 0-5, in increments of .5.

## <a name="struct"></a>Structure of dataset
Typically, the primary score shown by the sites will be the Critic score. Here are descriptions of some of the relevant columns in the dataset:

* FILM -- the name of the movie.
* RottenTomatoes -- the RottenTomatoes (RT) critic score.
* RottenTomatoes_User -- the RT user score.
* Metacritic -- the Metacritic critic score.
* Metacritic_User -- the Metacritic user score.
* IMDB -- the IMDB score given to the movie.
* Fandango_Stars -- the number of stars Fandango gave the movie.

To make it easier to compare scores across services, the columns were normalized so their scale and rounding matched the Fandango ratings. Any column with the suffix _norm is the corresponding column changed to a 0-5 scale. For example, RT_norm takes the RottenTomatoes column and turns it into a 0-5 scale from a 0-100 scale. Any column with the suffix _round is the rounded version of another column. For example, RT_user_norm_round rounds the RT_user_norm column to the nearest .5.

## ## <a name="goal"></a>Gaol of Analysis
