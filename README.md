# A Star Cast is Born: Striking Gold with the Perfect Lineup

## Abstract
In the art of filmmaking, a director's journey begins with casting, a critical choice that shapes a movie's soul and its path to success. Our study offers a beacon to directors, illuminating key aspects they should consider in their cast. Central to this quest is understanding the impact of gender and ethnicity diversity on audience and critical reception. Equally vital is discerning the ideal age for characters, ensuring authenticity and connection with viewers.

The narrative also explores the influence of actors' previous awards on a film's ratings. Can an accolade-laden cast elevate a movie's stature? Moreover, the interplay of relationships among actors is scrutinized, revealing how these dynamics can enhance or detract from a film's appeal.

Finally, our guide probes the balance between a cast's star power and the narrative depth of the film. It challenges directors to consider how well-known actors contribute to both the artistic depth and commercial viability of their projects, aiming for a harmonious blend that captivates both critics and audiences.

## Research Questions 🔎
In our project, we define the success of a movie in terms of IMDB ratings. To provide the perfect cast, we will analyse:
1. What impact do the `gender` and `ethnicity` of an actor have on the ratings of a movie?
2. What is the ideal `age` for a specific character type?
3. How does an actor's previous nomination or `award` affect the movie's ratings? 
4. How do `connections between actors` influence each other's contribution to movie ratings?
5. Is popularity everything? Do high ratings correspond to high `box-office revenue`?

## Additional Datasets 📈
1. IMDB [dataset](https://developer.imdb.com/non-commercial-datasets/): Ratings from IMDB. We are going to use the ratings as the dependent variable for our analysis. We merge it with each movie in the 'movie.metadata.csv' by combining by 'name' as unique key. As each movie appears multiple times we did a weighted average with the numbers of votes to have a general rating.
2. The Movies [dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?resource=download&select=movies_metadata.csv) for budgets, to isolate the influence of high rating in the 'box office revenue'.
3. Awards [dataset](https://datahub.io/rufuspollock/oscars-nominees-and-winners#resource-oscars-nominees-and-winners_zip): This dataset contains all the winners and the nominees of the Oscars since 1927. It will be used to gauge the actors academically so we merged it with the 'character.metadata.tsv' dataframe.
4. Actor popularity [dataset](https://today.yougov.com/ratings/entertainment/fame/all-time-actors-actresses/all): Fame, popularity, liked, disliked and neutral ratios among US population. (scrapped data)
5. Inflation [dataset](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?end=2022&start=1960&view=chart): Consumer prices increase since 1960. This dataset will be used to adjust (budget and) box office revenue of the movies, mostly for our last question.

## Methods 📊

### General Pre-Processing
  1. Movie Metadata:
  2. Character Metadata:

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
