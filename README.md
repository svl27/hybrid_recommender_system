# Hybrid Recommender System using Content-based Filtering and Collaborative-based Filtering
![Alt Text](https://repository-images.githubusercontent.com/275336521/20d38e00-6634-11eb-9d1f-6a5232d0f84f)https://repository-images.githubusercontent.com/275336521/20d38e00-6634-11eb-9d1f-6a5232d0f84f)

In this project, we build a hybrid movie recommender system using both content-based filtering and collaborative filtering techniques on the MovieLens dataset.

## Introduction

A recommender system is a tool that predicts a user's preferences or ratings for items. It's widely used in different online applications like e-commerce, streaming services, and social media. There are two main types of recommendation systems: content-based filtering and collaborative filtering. In this project, we combine both methods into a hybrid recommender system to take advantage of the strengths of both approaches.

## Installing Dependencies using pip

To run this project, you will need to install several Python libraries. You can install them using pip, which is a package manager for Python.

To install pip, follow the instructions [here](https://pip.pypa.io/en/stable/installation/). Once pip is installed, you can install the required libraries by running the following commands in your terminal:
```
pip install pandas
pip install numpy
pip install scikit-learn
pip install scipy
pip install matplotlib
pip install fuzzywuzzy
pip install python-Levenshtein
pip install seaborn
pip install datetime
pip install pillow
```
Note: If you encounter any issues while installing these packages, you might find it helpful to create a virtual environment. You can follow the instructions [here](https://docs.python.org/3/tutorial/venv.html) to set up a virtual environment in Python.

After installing these dependencies, you should be able to run the project by executing the Jupyter notebook.

Please ensure that you have Python 3.6 or newer installed. If you do not have Python installed, you can download it [here](https://www.python.org/downloads/).

You will also need to have Jupyter Notebook installed. If you don't have Jupyter installed, you can install it using pip:
```
pip install jupyter
```
After installing Jupyter, you can start the notebook server from the terminal:
```
jupyter notebook
```
This will open a web browser window. Navigate to the location of the project files to open the notebook.


## Installing Dependencies Using Poetry

[Poetry](https://python-poetry.org/) is a tool for dependency management and packaging in Python. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you.

First, you need to install Poetry. You can do this with the following command:
```
curl -sSL https://install.python-poetry.org | python -
```
This will install Poetry in your home directory. The installer will also modify your PATH variable so that the poetry command can be called from any shell session.

Next, navigate to your project directory in your terminal and create a new virtual environment with Poetry:
```
poetry shell
```
This will create a new virtual environment for your project, isolated from your system's Python environment.

To add necessary packages to your project, use the poetry add command followed by the package name. For example, to install the required packages for this project, you would run:
```
poetry add pandas numpy ipykernel scikit-learn scipy fuzzywuzzy matplotlib seaborn datetime pillow python-levenshtein 
```
This will add the packages to your pyproject.toml file and install them in your virtual environment.

Now, you're ready to run your Python scripts in the virtual environment that Poetry set up for you.

If you want to leave the virtual environment, simply type exit in your terminal.

Please note that every time you start a new terminal session, you will need to reactivate the virtual environment with poetry shell before you can run your scripts.

I have also included 'pyproject.toml' and 'poetry.lock' for your reference.

## Dataset

This data set contains 10000054 ratings and 95580 tags applied to 10681 movies by 71567 users of the online movie recommender service MovieLens.

Users were selected at random for inclusion. All users selected had rated at least 20 movies. Unlike previous MovieLens data sets, no demographic information is included. Each user is represented by an id, and no other information is provided.The data are contained in three files, movies.dat, ratings.dat and tags.dat.

More details about the contents and use of all these files is given in README HTML document in the dataset.

You can download the dataset from this link http://files.grouplens.org/datasets/movielens/ml-10m.zip

## Models

Our hybrid recommender system combines content-based filtering and collaborative filtering:

**Content-based filtering**: This method uses the cosine similarity between tf-idf vectors of movie descriptions to find similar movies. If a user liked a particular movie, the system will recommend movies that are similar in terms of their content (genres, tags, etc.).

**Collaborative filtering**: This method uses matrix factorization to predict a user's rating for a movie based on the ratings of similar users and/or similar movies. We use the Singular Value Decomposition (SVD) algorithm from the Surprise library for this purpose.

## Recommendation

Given a user ID and a favorite movie title, our system provides a list of recommended movies. These recommendations are generated through a hybrid function that combines content-based filtering and collaborative filtering. The content-based component considers movies similar to the user's favorite movie, while the collaborative component takes into account movies liked by users similar to the input user. The final recommendations are a weighted combination of these two approaches, tailored to both the user's specific tastes and broader user trends.

## Challenges

**Data Size**: The MovieLens dataset is quite large, especially when considering the full dataset with 27,000,000 ratings. This posed challenges in terms of memory usage and computational efficiency.

**Sparse Data**: The user-item interactions matrix is extremely sparse as not every user has rated every movie. This posed a challenge in terms of both storage and in building meaningful collaborative filtering models.

**Evaluation**: Recommender systems are hard to evaluate accurately. Traditional metrics such as precision and recall can be used, but they do not take into account the ranking of recommendations. More advanced metrics such as Normalized Discounted Cumulative Gain (NDCG) were needed.

**Feature Representation**: Representing movies for content-based filtering was challenging. The genres, tags, and other textual data had to be transformed into a numerical form for computations, and this required careful preprocessing and feature engineering.

**Model Tuning**: Tuning the models to get the optimal recommendations was another challenge. This included deciding the weightage given to content-based versus collaborative filtering models, the number of latent factors in the SVD model, and more.

## Future Improvements

This project is a starting point for building a more sophisticated recommender system. Potential future improvements include:

1. Implementing the recommender system in a distributed computing framework like PySpark to handle larger datasets.
2. Deploying the recommender system in a production environment, for example as a web service.
3. Incorporating more information (e.g., movie cast, director, user demographic information) into the recommendation algorithms.
4. Evaluating and optimizing the recommendation algorithms using offline evaluation, online A/B testing, and user feedback.














