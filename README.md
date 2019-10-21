
# Module 1- King County Data Set Project


## Introduction

In this repo, you will find the main Jupyter notebook labeled 'student.ipynb' where I have attempted to answer the question of house prices using data science, graphs, and statistics.  The main files are commented below in addition to a number of other files explaining the project.

* **student.ipynb** - Jupyter notebook file where the body of work is located
* **kc_house_data.csv** - The csv file with the King County data
* **Model_Attempts** -  The folder containing the numerous attempts at creating a valid regression
* **column_names.md** -  The file explain the column names that I have also included here
* **KingCountyMap.png** -  A map of King County - though I also used folium in the project
* **kingcountyzipcodes.pdf** -  A pdf of where the local zipcodes are, which was helpful for binning zones
* **README.md** -  The Readme file which you have found
* **LICENSE.md** -  The License file containing rights for me to work on this
* **CONTRIBUTING.md** -  The Contributing file showing all those who helped
* **Presentation.pdf** -  The non-technical slide show of my results


## The Dataset
The King County Dataset was presented to me as an introductory project to showcase all that I have learned in the first month with Flatiron Academy. I needed to clean, explore, and model this dataset using a multivariate linear regression in order to predict house sale prices.


# Column Names and descriptions for Kings County Data Set
* **id** - unique identified for a house
* **dateDate** - house was sold
* **pricePrice** -  is prediction target
* **bedroomsNumber** -  of Bedrooms/House
* **bathroomsNumber** -  of bathrooms/bedrooms
* **sqft_livingsquare** -  footage of the home
* **sqft_lotsquare** -  footage of the lot
* **floorsTotal** -  floors (levels) in house
* **waterfront** - House which has a view to a waterfront
* **view** - Has been viewed
* **condition** - How good the condition is ( Overall )
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house apart from basement
* **sqft_basement** - square footage of the basement
* **yr_built** - Built Year
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors

# Load all the libraries I know.
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
%matplotlib inline
import scipy.stats as stats
import statsmodels.api as sm
from statsmodels.formula.api import ols
import folium


# Column Names and Cleaning Techniques
### Below are a list of some of the techniques that I use to help get a better regression
* **id** Drop - categorical data, has no meaning
* **dateDate** Object - need to change format or categorize by month or year
* **pricePrice** - Independent Variable
* **bedroomsNumber** - Has an outlier of 33. Change this to the median '3'
* **bathroomsNumber** - Continuous but with outliers
* **sqft_livingsquare** - Continuous with outliers - could effect multicolinearity
* **sqft_lotsquare** - Continuous with outliers - could also effect multicolinearity
* **floorsTotal** - Categorical - bin
* **waterfront** - Categorical - Has missing data, lots of zeros - clean up and bin
* **viewed** - Categorical - Also has missing data - clean up and bin
* **condition** - Categorical - could be binned
* **grade** - Categorical - could be binned
* **sqft_above** - Continuous with outliers - could effect multilinearity, possibly going to drop
* **sqft_basement** - Object - has missing data, many "?" - clean and bin
* **yr_built** - Continuous
* **yr_renovated** - Continuous - Has lots of zeros - possibly going to bin
* **zipcode** - Categorical - bin based on location?
* **lat** - Continuous - bin based on location?
* **long** - Continuous - bin based on location?
* **sqft_living15** - Continuous but with outliers - also could effect multicoliniarity.
* **sqft_lot15** - Continuous but with outliers - also could effect multicoliniarity.


## Summary
After cleaning the data and creating numerous models I determined that there is still alot of Python code that I am struggling to understand. I very much enjoyed exploring the data, creating graphs, and building models (you can see that I built many of them). At the same time I learned a lot about this dataset and what it takes to really dig into each column and find missing values. I learned about more about binning, creating graphs, and doing log transformations!


## Contributing
Please read CONTRIBUTING.md for more details.

## Versioning
You will note in the Models_Attemp folder that I have tried many different versions of this notebook as it was easier for me to copy and start over instead of working on a single notebook.  Hopefully someday I will learn how to effectively use Github to branch, fork, and work off of a master.

## Authors
TJ Whipple - A Novice Data Scientist and Python Programmer
See also the list of contributors and instructors who put this project together.

## License
This project is licensed through Flatiron Academy - see the LICENSE.md file for details

## Acknowledgments
I just want to thank my advisor, Abhineet for all his support and suggestions throughout this project as well as all the members of my Flatiron September Cohort who were there for me.  Thank to Tim, Jose, and Aretha for your helpful code, sharing ideas, and strugging through this with me!



