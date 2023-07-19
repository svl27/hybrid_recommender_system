# Hybrid Recommender System using Content-based Filtering and Collaborative-based Filtering
![Alt Text](https://repository-images.githubusercontent.com/275336521/20d38e00-6634-11eb-9d1f-6a5232d0f84f)https://repository-images.githubusercontent.com/275336521/20d38e00-6634-11eb-9d1f-6a5232d0f84f)

In this project, we build a hybrid movie recommender system using both content-based filtering and collaborative filtering techniques on the MovieLens dataset.
## Introduction

A recommender system is a tool that predicts a user's preferences or ratings for items. It's widely used in different online applications like e-commerce, streaming services, and social media. There are two main types of recommendation systems: content-based filtering and collaborative filtering. In this project, we combine both methods into a hybrid recommender system to take advantage of the strengths of both approaches.

## Setup

This project requires several Python libraries for data analysis and machine learning, including pandas, numpy, scikit-learn, scipy, surprise, and fuzzywuzzy. You can install these libraries using pip:
```
pip install pandas numpy scikit-learn scipy surprise fuzzywuzzy matplotlib seaborn datetime python-levenshtein pillow 
```

You can also Python package to setup poetry as explained below. I have also included 'pyproject.toml' and 'poetry.lock' for your reference.

## Installing Packages Using Poetry

Poetry is a tool for dependency management and packaging in Python. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you.

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
poetry add pandas numpy scikit-learn scipy surprise fuzzywuzzy
```
This will add the packages to your pyproject.toml file and install them in your virtual environment.

Now, you're ready to run your Python scripts in the virtual environment that Poetry set up for you.

If you want to leave the virtual environment, simply type exit in your terminal.

Please note that every time you start a new terminal session, you will need to reactivate the virtual environment with poetry shell before you can run your scripts.


## Dataset

This data set contains 10000054 ratings and 95580 tags applied to 10681 movies by 71567 users of the online movie recommender service MovieLens.
You can download the dataset from this [link](“http://files.grouplens.org/datasets/movielens/ml-10m.zip).







