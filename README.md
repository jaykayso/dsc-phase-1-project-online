# Microsoft Movie Studios: Project One

### Our Objective

Microsoft sees all the big companies creating original video content, and they want to get in on the fun. They have decided to create a new movie studio, but the problem is they don’t know anything about creating movies. They have hired you to help them better understand the movie industry. Your team is charged with exploring what type of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

### The Data
Several files were made available from Box Office Mojo, Rotten Tomatoes, IMDB, and TheMovieDB.org. 


<details><summary style="font-size: 18px"> 
List of Files:</summary> 

```
|-bom.movie_gross.csv.gz
|-imdb.name.basics.csv.gz
|-imdb.title.akas.csv.gz
|-imdb.title.basics.csv.gz
|-imdb.title.crew.csv.gz
|-imdb.title.principals.csv.gz
|-imdb.title.ratings.csv.gz
|-rt.movie_info.tsv.gz
|-rt.reviews.tsv.gz
|-tmdb.movies.csv.gz
|-tn.movie_budgets.csv.gz
```
</details>
<!------------------------------------------>


### Exploratory Questions

[Question One Notebook Link](https://github.com/jaykayso/dsc-phase-1-project-online/blob/master/Question%201.ipynb)
<details><summary style="font-size: 24px">
Question 1: Which genres or themes get the highest ratings?

Data Used: 
    - imdb.title.ratings.csv
    - imdb.title.basics.csv
    
In order to properly calculate the rating average of each genre, I had to split the clusters of the genres so that each cell had one genre with one rating. Then, I was able to calculate the mean with the genres grouped. In conclusion, since Adult and Horror movies average the lowest in terms of rating, I would advise Microsoft agaist creating those movies. 
    
[Question Two Notebook Link](https://github.com/jaykayso/dsc-phase-1-project-online/blob/master/Question%202%20.ipynb)
<details><summary style="font-size: 24px">
Question 2: Does release date impact profit?

Data Used: 
    - tn.movie_budgets.csv
 
I calculated profit by subtracting production budget from the worldwide gross revenue. Then, I calculated profit margin by dividing the profit by the production budget. I grouped this profit margin in terms of weeks of the year and also days of the week to determine if a particular time of release day was more profitable. I quickly found out that sorting by day was mute since the vast majority of movies are released on Friday. Additionally, the highest weeks of movie releases were at the end of the year. The conclusion I drew here was that the movie industry is aware that demand for movies peaks at the end of the week and year. For Microsoft to be successful in the movie space, I would encourage them to take advantage of the peak demand times as well. 
    
[Question Three Notebook Link](https://github.com/jaykayso/dsc-phase-1-project-online/blob/master/Question%203.ipynb)
<details><summary style="font-size: 24px">
Question 3: Can we find writers that show a track record of writing well-rated movies?

Data Used: 
    - imdb.title.principals.csv
    - imdb.title.crew.csv
    - imdb.name.basics.csv
    - imdb.title.ratings.csv
    - imdb.title.basics.csv
    - imdb.title.akas.csv
    
Within the data, the tconst values represent the unique movie titles while the nconst values represent the unique crew names. I separated the clusteers of nconst values and set each to a unique tconst value. I restricted the data to only feature writers. Afterwards, I was able to join that dataframe with movie ratings and create a column that included the count of movies that a particular crew member (nconst) had done. I further restricted the dataframe to only include writers who had written over 5 movies. This made it possible to group by the nconst values (unique crew members) and determine what the average was for each individual writer. I attached the crew names to the short list of qualified writers. In conclusion, I would recommend that Microsoft Studios hire a writer with a track record of successful, highly rated, movies.
    
[Question Four Notebook Link](https://github.com/jaykayso/dsc-phase-1-project-online/blob/master/Question%204.ipynb)
<details><summary style="font-size: 24px">
Question 4: Can we find directors with a track record of directing well-rated movies?

    
 Data Used: 
    - imdb.title.principals.csv
    - imdb.title.crew.csv
    - imdb.name.basics.csv
    - imdb.title.ratings.csv
    - imdb.title.basics.csv
    - imdb.title.akas.csv
    
    
Within the data, the tconst values represent the unique movie titles while the nconst values represent the unique crew names. I separated the clusteers of nconst values and set each to a unique tconst value. I restricted the data to only feature writers. Afterwards, I was able to join that dataframe with movie ratings and create a column that included the count of movies that a particular crew member (nconst) had done. I further restricted the dataframe to only include directors who had directed over 5 movies. This made it possible to group by the nconst values (unique crew members) and determine what the average was for each individual director. I attached the crew names to the short list of qualified directors. In conclusion, I would recommend that Microsoft Studios hire a director with a track record of successful, highly rated, movies.  
    
    
# Wrap Up
    
Microsoft should release a movie on a Friday at the end of the year with a skilled director and writer, and they should avoid the genres of horror and adult. 
    
    
# Future Work
    
I recommend that we further investigate the connection to qualified crew members and movie success. Additionally, it would be interesting to look at a dataset on movie sales and demand on movies year round. 
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    