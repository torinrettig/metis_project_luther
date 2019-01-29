# Project Luther Proposal (alt) - Film Production Budget ROI

Analysis: Torin Rettig

### What factors contribute to the ROI of a film? 

### Proposal

Filmmaking is an expensive, high-stakes business and a tremendous amount of time, effort and resources are devoted to tracking a film's performance. While filmmakers want all of their films to be a breakout hit that has tremendous ROI, the first hurdle for revenues to clear is the cost to make the film. 

But what are the factors that contribute to a film's financial success? The budget of the film? The popularity of the actors? The number of articles written about it? In this analysis we will create a linear regression model that predicts what proportion of a film's budget will be recouped in revenue, and in optimizing the model we hope to discover the factors that most influence a film's financial fate. 

### Assumptions

- We will assume that the major factors that most affect ROI are the budget of the film, the initial performance of the film (opening weekend), film reviews, the revenue trend over the first month, and the principals (actors, directors) that are attached to the film. 
- We will also look at the MOVIEmeter rating, the ratings breakdown of the film, both in terms of the rating itself and the number of votes determining that rating. 

### Methodology

- Gather financial, cast, director, ratings and other details of films with a recorded budget and performance numbers that have been out for over 3 months. Most films end their theatrical run before this, so with this cutoff we can be relatively certain we've captured the relevant financial data. We will aim to capture the performance of over 1000 films.
- Gather actor popularity details  available through IMDb and other sites for the principals of these films.
- Build a linear regression to determine the factors that most greatly affect ROI on the film's budget.

### Data

- Target - Proportion of budget recouped through gross revenue.
- Features - Film financial performance numers. 
- Features - Film ratings breakdown and MOVIEmeter rating at opening.
- Features - STARmeter rating and other details of principal cast and directors. 
- Data Sources: IMDb

### Features

1. TARGET = Gross Revenue Proportion of Budget (Gross Revenue/Budget)
2. Production budget (IMDb) - (Integer)
3. Opening weekend gross  (IMDB) - (Integer)
4. US gross of film  (IMDb) - (Integer)

   - US gross: Release + 1Mo
   - US gross: Release + 2Mo
5. Foreign gross of film (IMDB) - (Integer)

   - International gross: Release + 1Mo
   - International gross: Release + 2Mo
6. Worldwide gross of film (IMDb) - (Integer)

   - Worldwide gross: Release + 1Mo
   - Worldwide gross: Release + 2Mo
7. __Mean US gross trend, week over week (IMDb) - (Float)__
8. __Mean Foreign gross trend, week over week (IMDb) - (Float)__
9. __Mean worldwide gross trend, week over week (IMDb) - (Float)__
10. MOVIEmeter rating at launch (Integer)
    - __MOVIEmeter rating: Release + 1Mo__
    - __MOVIEmeter rating: Release + 1Mo Trend__
11. Mean STARmeter rating of principal cast at launch:  (IMDb) (Float)
    - __Mean Instagram followers of principal cast__
    - __Instagram followers of principal cast with highest STARmeter__
    - __Mean Twitter followers of principal cast__
    - __Twitter followers of principal cast with highest STARmeter__
    - __Mean Age of principal cast__
    - __Age of principal cast with highest STARmeter__
12. Ratings Breakdown of film (IMDB) - (Float)
13. Ratings Breakdown number of votes (IMDb) - (Integer)
14. __Metacritic Rating (IMDb) - (Integer)__
15. Articles written about film (IMDb) - (Integer)
    - __Number of articles written prior to launch__
    - __Density of articles written prior to launch__
16. __Month of Release__
17. __Season of Release__

  ​    

    

### Prediction

ROI on production budget



