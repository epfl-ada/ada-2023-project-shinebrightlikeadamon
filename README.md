# From a Star Cast to a Cast that Brings Stars: What lies in between 

## Abstract

In the glitzy world of Hollywood, fame and fortune are everything. From the choice of the cast, to the country of production, to the outfit worn at the 56th minute, everything is done in order to maximize a movie's success. But in the 21st century, where an actor's Instagram following can earn them thousands of dollars per sponsored post, and where users can access the profiles of an actor's castmates and of their movie with just a few cliks, does fame have an impact of movie ratings? What about online popularity? Maybe these aspects overshadow the influece of renouned awards... The more famous actors in a movie, the better the ratings?
We go past mere talent, examining if an actor's fame and previous awards increase a movie's ratings: does having an award-winner or a star lead to better ratings? To add to this, we look into how connections between actors affect a movie's charm.
However shiny the ratings' stars may be, though, Hollywood is still, first and foremost, an industry looking to maximise its profit: we explore whether there exists a direct correlation between movie ratings and their revenue, and whether fame influences such revenue. 
From fame to fortune, we're about to unravel the thrilling mysteries that make the movie industry sparkle. 

## Research Questions 🤨
In our project, we define the success of a movie in terms of IMDB ratings. To provide the perfect cast, we will answer the following questions:

1. Do stars make movies shine brighter? How does `popularity`, a previous nomination or `award` received by an actor impact the ratings of a movie?
2. How do `connections between actors` influence each other's contribution to movie ratings?
3. Is popularity everything? Do high ratings correspond to high `box-office revenue`?

## Additional Datasets 💽
1. IMDB [dataset](https://developer.imdb.com/non-commercial-datasets/): Ratings from IMDB. We are going to use the ratings as the dependent variable for our analysis. We merge it with each movie in the `movie.metadata.csv` by `(name,release_year,runtime)` as unique key.
2. The Movies [dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?resource=download&select=movies_metadata.csv) for budgets, to isolate the influence of high rating in the `box office revenue`.
3. Awards [dataset](https://datahub.io/rufuspollock/oscars-nominees-and-winners#resource-oscars-nominees-and-winners_zip): containing all Oscars winners and nominees since 1927. It will be used to gauge the actors academically so we merged it with the `character.metadata.tsv` dataframe, to include actor's awards up to that movie.
4. Actor popularity [dataset](https://today.yougov.com/ratings/entertainment/fame/all-time-actors-actresses/all): `Fame`, `popularity`, `liked`, `disliked` and `neutral` ratios among US population (scrapped data).
5. Inflation [dataset](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?end=2022&start=1960&view=chart): Consumer prices increase since 1960. This dataset will be used to adjust `budget` and `box office revenue` of the movies.

## Methods 📊 

### Time Series Analysis:  
We use Time Series Analysis to examine how an actor's win or nomination for an award influences the ratings of their subsequent movies. 

We collect time-stamped data on the actor's award nominations/wins and the ratings of their movies (time-stamped with their release date) over time, resulting in one time series for the actor's awards and another for movie ratings, which we then perform Regression Analysis on.

### Paired Matching
We employed paired matching to examine potential causal relationships within observed correlations between time-stamped award nominations/wins and movie ratings. We standardized the continuous variables, calculated propensity scores and performed the matching. 

### Regression Analysis:
We apply Regression Analysis on the Time Series Analysis to determine how an actor's award win or nomination influences the ratings of their subsequent movies. 

### Network Analysis: 
By mapping out the connections between co-starring actors, we analyze if and how these networks correlate with movie ratings. This analysis can reveal influential actors whose connections might positively or negatively impact a movie's ratings. Representing the actors as nodes and their connections as edges, using degree centrality to measure the number of connections an actor has within a network to understand the actor's prominence or influence in the movie industry.    

### ANOVA (Analysis of Variance): 
We perform Analysis of Variance (an extension of the t-test used to compare the means of three or more groups) to compare the means of movie ratings from different communities of actors, after having conducted network analysis.

### Propensity Score 
@TimB

### Correlation Analysis: 
We perform Correlation Analysis, with Pearson's Correlation Coefficient, to find out if there's a statistical relationship ratings are box-office revenue. 

## Timeline ⏱️
![Shine Bright Like Adamon](img/timeline.png)

## Milestones 🗿

### 1. Data Processing and Preparation
- **Movie Metadata:**
  - Added average rating from the IMBD dataset, adjust box office revenue with inflation in the US from the additional dataset to be able to compare them, implemented budget values and adjust them like box office. We also added the size of the cast, the number of awards/nominations of the cast and its average popularity and experience.
- **Character Metadata:**
  - Includes all actor data adjusted to the release date of the movie: age, awards, experience.
- **Actor Data:**
  - Collected all the following data per actor:
    - Popularity, %liked, %disliked, %neutral in the US population.
    - Total number of movies made
    - Number of awards/nominations
    - General data as birth, gender, height and etnicity.	

### 2. Exploratory Data Analysis
- **Task 2.1:** Conduct descriptive statistical analysis to understand basic trends and distributions within the dataset.
- **Task 2.2:** Visualize key variables (awards, communities, revenue...) to gain initial insights and identify potential patterns or outliers.

### 3. Impact of Awards and Popularity
- **Task 3.1:** Use time series analysis to assess actor award history's impact on movie ratings.
- **Task 3.2:** Use correlation analysis to explore actor popularity's impact on movie ratings.

### 4. Network Analysis of Actor Connections
- **Task 4.1:** Create a network graph of actors based on their co-starring roles.
- **Task 4.2:** Apply correlation analysis to assess how connections between actors affect movie ratings.
- **Task 4.3:** Compute the propensity score to explore causality between movie genre and movie ratings.     @TimB

### 5. Relationship Between Ratings, Revenue, and Budget
- **Task 5.1:**  Study the relationship between movie ratings and box office revenue while considering budget data for a comprehensive analysis of financial performance.
- **Task 5.2:**  Employ regression analysis to assess the impact of ratings on box-office revenue, controlling for movie budgets to determine their influence.
- **Task 5.3:**  Perform comparative analysis to evaluate if movies with similar budgets but varying ratings have different revenue outcomes, further underscoring the role of ratings in financial success.

### 6. Development of Frontend for Data Visualization
- **Task 6.1:** Create an interactive frontend website for visualizing key data findings through charts and graphs.
- **Task 6.2:** Ensure user-friendliness, accessibility, and clear data presentation in the website's design.
- **Task 6.3:** Test the website for functionality and user experience.

## Team Organization 👨‍👩‍👧‍👦
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
      <td>README.md: Questions, Methods, Timeline, Team Organization</td>
    </tr>
    <tr>
      <td>Félix</td>
      <td>Scraping of actors popularity dataset, methods and initial data merging</td>
    </tr>
    <tr>
      <td>Marine</td>
      <td>README.md: Abstract, Questions, Methods, Milestones</td>
    </tr>
    <tr>
      <td>Tim B.</td>
      <td>Data pre-processing</td>
    </tr>
    <tr>
      <td>Tim W.</td>
      <td>Collection of datasets, Milestones, Front-End setup</td>
    </tr>
  </table>

</body>
</html>
