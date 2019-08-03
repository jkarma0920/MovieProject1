# Movie Analysis on Different Genres and Profitability
Contributors: Jay Kim, Jon Bebi and Marco Santos

## Task:
Film ideas for a prospective movie studio, given:
 * Industry Landscape
 * SWOT Analysis
 * Current Trends
Findings evidenced by Graphs & Tables

## Applications Utilized:
Data Science Tools Used:
 * GitHub
 * Jupyter Notebook (Python)
 * MySQL
 * Beautiful Soup
 * Matplotlib

Websites Used:
 * Box Office Mojo (webscraping): $ metrics
 * IMDb (API): user ratings
 * The Numbers (webscraping): bankability of top industry figures

## How a movie's success is measured
A films success is dependant on multiple factors:
 * User Reviews
 * Box Office Performance
 * Returns relative to the budget
The following information presents discoveries showing which factor is most important when determining a film's profitability.
## Genres examined:
* 3D
* Animation
* Gay/Lesbian
* Horror
* Rom-Com

These genres were found from BoxOfficeMojo sorted by quantity of movies.  The other two genres ahead of the ones selected were Foreign Language and Documentary which were eliminated based on lack of overall mainstream success.

## MySQL Database schema with movies collected
Collected 715 Movies from BoxOfficeMojo and here it is being displayed as a summary table.

## Correlation between profit and ratings
![scatter](Images/profit_ratings_relation.png "Profit and ratings scatter plot")

A positive correlation is expected to have the scatter plot dots increasing from the left to right forming a gradual slope. Based on the data the result appears to be a nearly flat slope.  This displays no significant correlation between user reviews and box office revenue.

## Average budget and profit by genre
![bar](Images/budget_profit_by_genre.png "Average budget and profit bars")

For the genres of Rom-Com, Horror ang Gay/Lesbian the average profit is almost half of the average budget used. The average budget for this genres is relatively much lower than 3D and Animation.
