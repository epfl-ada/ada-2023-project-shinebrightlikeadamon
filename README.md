# A Star Cast is Born: Striking Gold with the Perfect Lineup

## Abstract
In the art of filmmaking, a director's journey begins with casting, a critical choice that shapes a movie's soul and its path to success. Our study offers a beacon to directors, illuminating key aspects they should consider in their cast. Central to this quest is understanding the impact of gender and ethnicity diversity on audience and critical reception. Equally vital is discerning the ideal age for characters, ensuring authenticity and connection with viewers.

The narrative also explores the influence of actors' previous awards on a film's ratings. Can an accolade-laden cast elevate a movie's stature? Moreover, the interplay of relationships among actors is scrutinized, revealing how these dynamics can enhance or detract from a film's appeal.

Finally, our guide probes the balance between a cast's star power and the narrative depth of the film. It challenges directors to consider how well-known actors contribute to both the artistic depth and commercial viability of their projects, aiming for a harmonious blend that captivates both critics and audiences.

## Research Questions 🔎
In our project, we define the success of a movie in terms of IMDB ratings. To provide the perfect cast, we will answer the following five questions:

1. How does an actor's `gender` and `ethnicity` influence the ratings of a film?
2. What is the optimal `age` for portraying specific character types?
3. How does a previous nomination or `award` received by an actor impact the ratings of a movie?
4. How do `connections between actors` influence each other's contribution to movie ratings?
5. Is popularity everything? Do high ratings correspond to high `box-office revenue`?

## Additional Datasets 📈
1. IMDB [dataset](https://developer.imdb.com/non-commercial-datasets/): This dataset contains the IMDB ratings for each movie which we will use to measure a movie’s success. 
2. The Budget [dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?resource=download&select=movies_metadata.csv)
3. Awards [dataset](https://datahub.io/rufuspollock/oscars-nominees-and-winners#resource-oscars-nominees-and-winners_zip): This dataset contains all the winners and the nominees of the Oscars since 1927. It will be used to gauge the actors academically.
4. Actor popularity [dataset](https://github.com/): A dataset containing the fame, popularity, dislike percentage for actors.
5. Inflation [dataset](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?end=2022&start=1960&view=chart): Consumer prices increase since 1960. This dataset will be used to adjust (budget and) box office revenue of the movies.

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
