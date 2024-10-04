<p align="center">
<img src="Presentation/Images/header.jpg" width=1000px>
</p>

# Flatiron Studio
## Overview

Our company, Microwave Ovens and More, is venturing into film making.  When Amazon and Apple started distributing films, they turned to established movie studios to produce their films.  Given the talent and expertise at these studios, it would make sense to follow a similar path.  To support this, this data analysis explored the business side of large American movie studios and found these key insights:

1. Even **lower-budget** films produced for **under $12 million** can turn a **profit**.
2. **Universal Pictures**, **Columbia Pictures**, and **Paramount Studios** have been the most financially successful with these lower-budget films.  
3. These three studios have produced many profitable, well-reviewed **comedies** and **dramas** at these lower-budgets.

## Business Problem
This data analysis sought to understand the financial side of major American studios in order to evaluate a potential partnership with them.  It looked to answer these three questions:  
1. What are the typical range of production budgets for a movie at a major studio, and what size return on investment could be expected?
2. Which studios are financially successful in our budget-range?  
3. What genre of movie have these studios been successful with?  

Two metrics have been used to measure movie success:
- **Return on Investment**: movie profit/movie budget
- **Percent Fresh**: the fraction of good reviews given to a movie, as compiled by Rotten Tomatoes

## Data Understanding  
The data was drawn from a TMDB Dataset of 1 million records details movies released from the 1930s to 2024.  The data was collected by [The Movie Database](http://tmdb.org) and posted to [Kaggle](https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies).   

## Data Preparation
These were the key features used from the TMDB dataset:
- Release Date
- Movie Title
- Production Budget
- Revenue
- Production Company
- Genre
- Production Country

From Rotten Tomatoes:
- Freshness Rating for each review
- Box Office Returns

### Drop NaN Values and Fix Production Companies/Genres
First, import the TMDB dataset, and drop rows missing budget, revenue, and production company data.  Also, drop films with budgets below $100,000, as this is probably errant data.


## Analyze Data
### Visualization 1: Production Budgets and ROIs at Top Studios

The top American movie studios produce films with budgets from just a few hundred thousand dollars to hundreds of millions of dollars.  In the graphs below, we see that the films costing **less that $12 million** are well represented.  Half of these films turn a profit.  For our first forays into movie making, producing a film with a budget under $12 million makes sense.  
<img src="Presentation/Images/overview_studios.png" width=1000px>

### Visualization 2: Top Studios for Lower-Budget Films
For films costing less than $12 million, we see that **Paramount Pictures**, **Columbia Pictures**, and **Universal Studios** have the highest ROIs.  
<img src="Presentation/Images/roi_studio_low_budget.png" width=500px>

### Visualization 3: Successful Genres For Low-Budget Films at Our Target Studios
A majority of the profitable films with budgets under $12 million at these three studios are either a **comedy** or **drama**.  
<img src="Presentation/Images/Genre_Count.png" width=500px>

### Visualization 4: How are quality and profit related?
Paramount, Columbia, and Universal comedy and drama films have a low-correlation between quality and revenue.  Here the average freshness score assigned by Rotten Tomatoes is a proxy for quality, and box-office is our revenue.  
<img src="Presentation/Images/freshBool_boxOffice.png" width=500px>

## Conclusions
1. **Lower-budget** films produced for **under $12 million** can turn a **profit**.
2. **Universal Pictures**, **Columbia Pictures**, and **Paramount Studios** have been the most financially successful with these lower-budget films.  
3. These three studios have produced many profitable, well-reviewed **comedies** and **dramas** at these lower-budgets.

## Next Steps
- Complete statistical significance tests to see if our target studios are likely to be different from the other American studios.
- Research other companies experience with investments in the film industry