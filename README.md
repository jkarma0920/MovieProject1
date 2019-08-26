# Exploratory Data Analysis on Film Industry: Genres and Profitability
Contributors: Jay Kim, Jon Bebi, and Marco Santos

## Task:
Film ideas for a prospective movie studio, given:
* Industry Landscape
* SWOT Analysis
* Current Trends
Findings evidenced by Graphs & Tables

## Applications Utilized:
Data Science Tools Used:
* Amazon Web Services (RDS, DB instances)
* Jupyter Notebook (Python)
* MySQL
* Beautiful Soup
* Matplotlib

Websites Used:
* Box Office Mojo (webscraping): $ metrics
* IMDb (API): user ratings
* The Numbers (webscraping): bankability of top industry figures

## How a movie's success is measured
A film's success is dependant on multiple factors:
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

These genres were found from BoxOfficeMojo sorted by quantity of movies.  The other two genres ahead of those selected were Foreign Language and Documentary, both of which were eliminated based on lack of overall mainstream success.

## MySQL Database schema with movies collected
![mainsqltable](Images/MainDB_Table_Head.png "Main SQL Table")
Collected 715 movies from BoxOfficeMojo, the beginning of which is displayed as a summary table above.  These movies' release dates spanned the years from 1980 (which was as far back as BoxOfficeMojo would allow) to the present.  The selected attributes from each film were scanned and uploaded using Python's MySQLconnector and a sequence of query commands.  The data was hosted on Amazon Web Services: Relational Database Servers, DB instances.

![the-numbers-webscraping-slide](Images/The-Numbers-Webscrape.png "Webscraping Example From Presentation")


## Data Collected and Visualized
The data gathered from both the-numbers.com and boxofficemojo.com were scraped using Python's Beautifulsoup library to parse through each website's HTML code.  An API key from OMDb, a third-party, through Python was used to gather the required user reviews from IMDb.com. The data was then visualized into various graphs and charts using Python's Matplotlib library.

## Correlation between profit and ratings
![scatter](Images/profit_ratings_relation.png "Profit And Ratings Scatter Plot")

A positive correlation is expected with scatter plot markers increasing from the left to right, forming a gradual slope upwards. Based on the data, however, the results appears to be at a nearly-flat slope (above).  This demonstrates little to no significant correlation between user reviews and box office revenue.
Adding the bankability metrics, however, adds further color to the relationship (below).  The Gay/Lesbian Genre nearly completely lacks presence in th top 50 star index, while the 3D category notably dominates, especially for big-budget blockbusters (like Avengers: Endgame in the upper-right).
![scatter](Images/ScatterPlot-Cross-Relationships.png "Scatter Plot With Bankability Marker Sizes")

## Average budget and profit by genre
![bar](Images/budget_profit_by_genre.png "Average Budget And Profit Bars")

For the genres of Rom-Com, Horror, and Gay/Lesbian the average profit is almost half of the average budget used. The average budget for this genres is relatively much lower than 3D and Animation.

## Average Multiplier vs. Average Profit

The average multiplier is simply calculated as the box office returns divided by the budget, showing how much return is expected on average given a movie's genre.  Even though the average profit return is nearly half of the average budget for Rom-Com, Horror, and Gay/Lesbian films; the profit gross is still not as high as the 3D or Animation genres.

![multivsprofit](Images/MultiVsProfit.png "Average Multiplier VS Average Profit")

This bar chart displays the multiplier vs the return and it can be observed that the Gay/Lesbian and Horror films have the best multiplier.  However, their respective profit does not return as much as the 3D and Animation genres.

## Histogram Distribution of Profitable Films across each Genre

![hist](Images/ChancesOfProfit.png "Histogram Distribution Of Films")

When it comes to the overall probability to making profitable movies, the likelihood a film studio can actually make a profit is shown above.  Most films across the genres are more likely to either break-even or lose money.  Only a few movies are able to make a decent profit in the film industry.

## Recommendations and Suggestions

Based on the visualized data, the recommended route for a brand new movie studio is to _focus primarily_ on __Gay/Lesbian themed movies or Horror films__.  Both of these genres provide a decent amount of profit without the large budget commitment a 3D or Animation movie requires.  Although, if a new film studio wanted to _make a large profit_, _break the box office_, and has no issue with investing a large amount of money in a film, it is recommended to focus on a __3D or Animation movie__ involving a __well-known, reputable industry professional__.  _At the very least_, involve a __famous actor/actress, or producer/director__ in a film in order to _increase the chances of making a profit_.  However, based on the distribution of profitable movies across the genres, it is suggested to not enter the film industry because _there is a larger chance of not making a profit at all_.
