# Video Game Sales Analysis

### An exploration of how genres sell compared to each other and the change in sales across years

1. Data 

	The dataset used for this analysis was scraped from vgchartz.com, with a BeautifulSoup script written and posted by Kaggle user Gregory Smith. The Kaggle host can be found [here](https://www.kaggle.com/gregorut/videogamesales), and the GitHub repository for the webscraper can be found [here](https://github.com/GregorUT/vgchartzScrape). This dataset contains ample categorical variables, such as platform of release, game genre, year of release, and the games' publishers. There are three continuous variable, units sold per game, that comes in three flavors, North American sales, European sales, and Japanese sales. With all of these features, the influence of genre, year, and publisher on sales can be investiagted, as well as any differences in the sales between the regions. 
	
2. Research Design
	
	For this analysis, the goal will be to identify which, if any, genres of games sell better than the others. If a genre is more popular, then it's median North American sales per game will be higher than other genres. Only games from the year 2000 to 2019 will be considered. Entries before 2000 are before the release and maturation of modern consoles, while there was only a single entry for the year 2020. The game Wii Sports has specifically been discarded. The sales numbers are immutably skewed, but Wii sports is an outlier amongst outliers, having been shipped with the Wii console. [Wii Sports has a well documented influence on gaming by emphasizing accesibility,](https://www.gamespot.com/articles/the-most-influential-games-of-the-21st-century-wii/1100-6466810/#:~:text=Like%20the%20Wii%2C%20it%20focused,the%20industry%20would%20approach%20accessibility.) so insight is not lost while making the Sports genre have a more comparable distribution to the other genres. To test this hypothesis, the data has been filtered by year and split by genre. With non-normal distributions and 12 genres,a Kruskal-Wallis test will be performed to detect any differences, followed by Mann-Whitney U tests to determine specific differences, and a Common Language Effect Size will be used to quantify any differences found. This second testing will focus on the best selling genres versus the worst selling genres.

	All p-values will be corrected for multiple testing to control the Type 1 error rate.
	
3. Audience
	
	The above analysis will offer insight to all stages of game production. Developers will be able to use the anlaysis of sales by genre to decide what elements of a more popular genre they might include in a new game of a less popular genre, hopefully increasing appeal and sales. Publishers will be interested in the anlaysis, to either prioritize more popular genres, or tap into the greater potential market for less popular genres of games. This research is meant to empower innovation and publishing to targetedly make decisions that drive sales.