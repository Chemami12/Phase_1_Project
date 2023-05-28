
#MICROSOFT MOVIE CREATION
## INTODUCTION

Microsoft is a company that was created in 1981 by Bill Gates and Paul Allen. It is the largest vendor of computer software in the world. It is also a leading provider of cloud computer services, video games, computer and gaming hardware.
With all its diversity across different fields. Its looking to venture into movie creation which has become a great sensation for big companies to create original video contents.

Video content are films, television, music etc. These production companies provuce these contents through various stages from pre-production to post production. They include script development, market research, pitch to distributors, casting, hair & make-up, custome, buy/renting equipments and editing of content.

Movies produced by big companies can reach the global market because the profit of each movies that they sell go into the production budget. The production budget caters for evertything in the movie.

It is important to identify a niche to which type of content should be created. The best known companies produce a specific type of content. This enables the company to perfect that area as opposed to having a general portfolio.
It is important to do research into the companies that are there and what they focus on and if there are gaps that microsoft can fill.

Since it is a new area for microsoft to venture into. It is essential for them to have key persinnel to start of with. THey are: Development executive- for creating good scripts,
Production supervisor - to ensure stick to schedule and budget,
Post-production supervisor - for editing the content and ensure deadlines are met and
Head of sales and distribution - for distribution of the produced content.

##PROBLEM STATEMENT
Microsoft has been the leading computer software distributors in the world. Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. Microsoft does not have any knowledge about movie creation as it is not an area they have ever ventured into before. It would be of great benefit if it would be able to know what it entails in terms of the production company, genre of film, having a star in the film, producers and the run-time of the movie to make a successful movie studio. The goal is to explore what types of films are currently the best at the box office. This will provide the CEO with tangible evidence on the type of films to create.

##MAIN OBJECTIVE
To identify the type of movies that are doing well in the box office.

###SPECIFIC OBJECTIVE
1. Identify the top performing films in the box office.
2. Identify the top performing films in terms of gross income.
3. The relationship between studio and total revenue for film.
4. Identify the most used studios.

##DATA FOR ANALYSIS
Data was extracted from the following sources:
Box Office Mojo
Rotten Tomatoes
TheMovieDB

##We have to import the following libraries to aid in our code writing and visualizations.
import pandas as pd
 import numpy as np
 import seaborn as sns
 import sqlite3 
 import matplotlib.pyplot as plt
 %matplotlib inline

 1. We are interested with the top performing films in terms of gross income. We will therefore filter our data to the films gener bom_df = pd.read_csv('bom.movie_gross.csv.gz') # load the csv file and assign it to a variable called bom_df

 Run commands to view information about the data frame
 bom_df.info
 
 Filtering data so as to get those that made more than $100,000,000 domestic gross revenue
 bom_df = bom_df[bom_df['domestic_gross'] > 100000000]
 bom_df

Identify the most sought after studio
bom_df.studio.value_counts()

Create histogram to show the how frequent a studio has been used
Fig, ax = plt.subplots(figsize = (20,8))
ax.hist(bom_df.studio, bins = 80, color= 'teal')
ax.set_xlabel('Studio')
ax.set_ylabel('Number of times the studio has been used')
ax.set_title('Studio counts')

2. We are interested with the top performing films in terms of popularity. We will therefore filter our data to the films gener bom_df = pd.read_csv('tmdb.movies.csv.gz') # load the csv file and assign it to a variable called tmdb_df

Run command to remove Unnamed 0 column
tmdb_df = pd.read_csv('tmdb.movies.csv.gz', index_col=0)
tmdb_df.head(20)

Identify the most popular top 20 movie titles by populaity
tmdb_df = tmdb_df.sort_values(by='popularity', ascending=False)
tmdb_df.head(20)

Plot histogram to show the most popular movie
Fig, ax = plt.subplots(figsize = (30,10))
ax.hist(tmdb_df.title, bins = 80)
ax.set_xlabel('title')
ax.set_ylabel('popularity')
ax.set_title('Most popular Movies')

3. We are interested with the top performing films in terms of popularity. We will therefore filter our data to the films gener bom_df = pd.read_csv('rt.movie_info.tsv.gz') # load the csv file and assign it to a variable called rt_df

Create a data frame with the crucial columns
rt_df = rt_df.loc[:, ['id', 'synopsis', 'rating', 'genre', 'director', 'writer', 'currency', 'box_office', 'runtime', 'studio']].head(20)
rt_df

Most revenue made at the box office
rt_df.box_office

Frequently used studios
rt_df.studio

Bar chart showing the relationship between studio and box office revenues
fig, ax = plt.subplots(figsize = (20,8))
ax.bar(x = rt_df['studio'], height= rt_df['box_office'])
ax.set_xlabel('studio')
ax.set_ylabel('box_office')
ax.set_title('Relationship between studio and box_office');

How different genres perform in the box office
fig, ax = plt.subplots(figsize=(20,8))
plt.barh(rt_df['genre'], width= rt_df['box_office'])
ax.set_title('How the genre of movie perform in the box office')
ax.set_ylabel('genre')
ax.set_xlabel('box office');


