# Recommondations with IBM Module

### Libraries Used
Pythin 3.6

Pandas

Numpy

Matplotlib

pickle


### Introduction
The purpose of this project was to create a recommendation engine for user regarding the articles that they each interact with. This recommendation engine implements FunkSVD and recommends articles for users.

#### I Exploratory Data Analysis
Explored the data given. Discovered information such like the number of unique articles that have an interaction with a user, and the number of unique articles in the dataset (whether they have any interactions or not), etc.

#### II Ranked-Based Recommendations
In order to find the most popular articles to recommend, an assumption was made that the most popular articles are those with the most interactions. These articles would then be the ones we would reccomend to new users or recurring ones.

#### III User-User Based Collaborative Filtering
To make more efficient recommendations, we could find users that are similar by the articles that they have interacted with.

#### IV Matrix Factorization
Here, matrix factorization was used in order to make article recommendations to the users on the IBM Watson Studio platform.

### Findings

Note that the user_item_matrix contains user ids as rows and article ids on the columns with 1 values where a user interacted with 
an article and a 0 otherwise.

When we run the model on the user_item_matrix, we get the following chart:

<img src="https://github.com/andrew-alarcon17/Recommondations_with_IBM/blob/main/Images/Training.png" width="500">


However, when we split the user_item_matrix into training and testing sets, we get this as a chart for the testing set:

<img src="https://github.com/andrew-alarcon17/Recommondations_with_IBM/blob/main/Images/Testing.png" width="500">

It is important to note that as we have more latent features, the lower our accuracy becomes. As more features are added, then the more our model becomes overfitted.
