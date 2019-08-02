# Movie Analysis on Different Genres and Profitability
Contributors: Marco Santos, Jon Bebi, and Jay Kim

## Task:
Film ideas for a prospective movie studio, given:
 * Industry Landscape
 * SWOT Analysis
 * Current Trends
Findings evidenced by Graphs & Tables

## Applications Utilized:
Data Science Tools Used:
 * github
 * Jupyter Notebook (running Python)
 * MySQL
 * Beautiful Soup
 * matplotlib

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
* Romantic Comedy
* Horror
* Gay/Lesbian

These genres were found from BoxOfficeMojo sorted by quantity of movies.  The other two genres ahead of the ones selected were Foreign Language and Documentary which were eliminated based on lack of overall mainstream success.

## MySQL Database Schema with movies collected
Collected 715 Movies from BoxOfficeMojo and here it is being displayed as a summary table.

## Correlation between a Film's Profit and it's ratings
![Cor](Images/profit_ratings_relation.png)

A positive correlation is expected to have the scatter plot points steadily increasing from the left to right forming a gradual slope.  Instead we have what appears to be a nearly flat slope.  This displays no significant correlation between user reviews and box office revenue.  
