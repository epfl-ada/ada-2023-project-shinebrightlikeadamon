# A Star Cast is Born: Striking Gold with the Perfect Lineup

## Abstract
In the art of filmmaking, a director’s work begins with the cast, a critical choice that shapes the future success of the movie. Our project offers a recommendation to directors, illuminating key aspects they should consider in their cast. Central to this research is understanding the impact of gender and diversity ratio on audience and critical reception. Another important aspect is the ideal age for characters, which ensures authenticity and believability to viewers. 

The narrative also explores the influence of actors' previous awards on a film's ratings. Can an award-winning cast elevate a movie’s rating? Furthermore, we will explore how the relationships between actors can enhance or detract from a film’s appeal.

Finally, our guide brings everything together for directors seeking to craft the ultimate cast to create a movie that's not just good, but one that tops the rating charts.

## Research Questions 🔎
In our project, we define the success of a movie in terms of IMDB ratings. To provide the perfect cast, we will answer the following five questions:

1. How does an actor's `gender` and `ethnicity` influence the ratings of a film?
2. What is the optimal `age` for portraying specific character types?
3. How does a previous nomination or `award` received by an actor impact the ratings of a movie?
4. How do `connections between actors` influence each other's contribution to movie ratings?
5. Is popularity everything? Do high ratings correspond to high `box-office revenue`?

## Additional Datasets 📈
1. IMDB [dataset](https://developer.imdb.com/non-commercial-datasets/): Ratings from IMDB. We are going to use the ratings as the dependent variable for our analysis. We merge it with each movie in the 'movie.metadata.csv' by combining by 'name' as unique key. As each movie appears multiple times we did a weighted average with the numbers of votes to have a general rating.
2. The Movies [dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?resource=download&select=movies_metadata.csv) for budgets, to isolate the influence of high rating in the 'box office revenue'.
3. Awards [dataset](https://datahub.io/rufuspollock/oscars-nominees-and-winners#resource-oscars-nominees-and-winners_zip): This dataset contains all the winners and the nominees of the Oscars since 1927. It will be used to gauge the actors academically so we merged it with the 'character.metadata.tsv' dataframe.
4. Actor popularity [dataset](https://today.yougov.com/ratings/entertainment/fame/all-time-actors-actresses/all): Fame, popularity, liked, disliked and neutral ratios among US population. (scrapped data)
5. Inflation [dataset](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?end=2022&start=1960&view=chart): Consumer prices increase since 1960. This dataset will be used to adjust (budget and) box office revenue of the movies, mostly for our last question.

## Methods 📊

### Regression Analysis:
Use linear or logistic regression to determine if there's a correlation between the gender and ethnicity of an actor and movie ratings. Can also be used to create models to predict box-office revenue based on movie ratings and other factors.

### ANOVA (Analysis of Variance): 
This can help in comparing the means of movie ratings across different groups of actors based on gender and ethnicity.

### Cluster Analysis: 
Group movies based on character types and analyze the age distribution of actors in these roles to identify trends.

### Descriptive Statistics: 
Calculate mean, median, and mode for ages of actors in different character types to determine the 'ideal' age.

### Time Series Analysis: 
Analyze how an actor's win or nomination in awards influences the ratings of their subsequent movies.

### Correlation Analysis: 
To find out if there's a statistical relationship between actors' connections and the ratings of movies they're in and to determine if high ratings are associated with high box-office revenue.

### General Pre-Processing
  1. Movie Metadata:
    - 
  2. Character Metadata:
    -

## Timeline ⌛️
![Shine Bright Like Adamon](img/timeline.png)

## Team Organization ✅
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

  <table>
    <tr>
      <th>Member</th>
      <th>Tasks</th>
    </tr>
    <tr>
      <td>Emma</td>
      <td>README.md: Questions, Timeline, Team Organization</td>
    </tr>
    <tr>
      <td>Félix</td>
      <td>scraping of actors popularity dataset, methods and initial data merging</td>
    </tr>
    <tr>
      <td>Marine</td>
      <td>README.md: Abstract</td>
    </tr>
    <tr>
      <td>Tim B.</td>
      <td>data pre-processing</td>
    </tr>
    <tr>
      <td>Tim W.</td>
      <td>collection of datasets</td>
    </tr>
  </table>

</body>
</html>


## Questions for TA ❔
