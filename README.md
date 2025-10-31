# VAR Impact on Home Advantage in Football
## Project Overview
This project aims to analyze the impact of the introduction of the Video Assistant Referee (VAR) system on home advantage in football. By comparing data such as home-win rates, goals, and referee decisions across the top five European leagues and the Turkish Süper Lig between the 2014–2015 and 2024–2025 seasons, the study investigates how VAR has influenced league dynamics specific to home-field advantage. The purpose is to identify whether the presence of VAR has reduced referee bias and changed psychological or fairness-related aspects of football matches.
## Motivation
VAR represents one of the most significant technological shifts in football. As football is a globally influential sport, understanding how this system has affected the game is both culturally and analytically valuable. Therefore, this project seeks to reveal VAR’s effectiveness in reshaping the patterns that have traditionally favored home teams.
## Research Questions
* Has home advantage decreased since the introduction of VAR?
	* Has there been a significant decline in home-win rates following the implementation of VAR?
	* How has VAR affected performance indicators such as points, goals, and expected goals (xG) for home and away teams?
	* Has the use of VAR influenced referee decisions in a way that reduces the traditional advantage of home teams?
* Does the impact of VAR on home advantage vary across leagues?
* How has the correlation between home points and final league ranking changed after VAR?
## Datasets  
The datasets for this project will be obtained from the following publicly available sources:

**1- StatHead by Sports Reference:** A comprehensive football statistics platform providing season, team and match-level data (accessed via subscription). 

Included variables:<br/>
	- Home and away match counts  
	- Wins, draws, losses (and win/draw/loss ratios) at home and away  
	- Average points per match (home / away)  
	- Final league ranking
	- Goals scored and conceded per 90 minutes (home / away)  
	- Expected Goals (xG) averages (home / away)    
	- Penalties awarded and conceded (home / away)  
  
[Link for StatHead (1. Dataset)](https://stathead.com/fbref/)  

**2- Club Football Match Data (2000 – 2025) – Kaggle:** An open dataset from Kaggle, containing match-level data across many leagues and seasons.  

Included variables:  
	- Fouls awarded and conceded (home / away)  
	- Yellow cards awarded and conceded (home / away)  
	- Red cards awarded and conceded (home / away)  
  
[Link for Kaggle (2. Dataset)](https://www.kaggle.com/datasets/adamgbor/club-football-match-data-2000-2025)  

*The datasets cover more than six leagues and span the years 2014–15 to 2024–25, but this project will focus only on that specific period and those six leagues.*
## Data Collection and Data Analysis Plan
### Data Collection
- **Dataset 1:** Downloading team and season-level data separately and merging them properly into the main dataset.
- **Dataset 2:** Downloading match-level data and converting them to the season level for each team.
- **Cleaning and Standardizing:** Aligning column names, formats, and variable types and applying necessary numeric conversions.
- **Missing Values:** Attempting to obtain missing information from external sources and, if not possible, considering methods such as interpolation or exclusion.
- **Merging:** Combining all data using a unique season–team identifier to construct the primary analysis table.
### Data Analysis
#### Exploratory Data Analysis
- Analyzing changes in home-advantage metrics before and after VAR, both overall and by league.
- Visualizing patterns, anomalies, and relationships using line plots, bar charts, heatmaps, and correlation matrices.
- Observing long-term trends through time-series and league-based visualizations.
#### Hypothesis Testing
- **H₀:** The implementation of VAR is not significantly affecting home advantage.
- **H₁:** The implementation of VAR is significantly reducing home advantage.
#### Comparative Analysis
- Comparing the effect of VAR across different leagues.
- Determining in which leagues the change is more noticeable.
## Estimated Sample Data
After the required datasets are cleaned, merged, and adapted to the project, the dataset is expected to look as follows (*this table is a simplified and condensed preview created for illustration purposes, and all values are hypothetical*):
|id   |team             |country|league        |season_start|season_end|home_w|xg_h|pen_h|≈49|
|-----|-----------------|-------|--------------|------------|----------|------|-------|-----|---|
|1    |Beşiktaş         |Türkiye|Süper Lig     |2014        |2015      |17    |11     |4    |…  |
|2    |Real Madrid      |Spain  |La Liga       |2014        |2015      |19    |16     |2    |…  |
|…    |…                |…      |…             |…           |…         |…     |…      |…    |…  |
|≈1281|Manchester United|England|Premier League|2024        |2025      |19    |11     |5    |…  |

### Glossary
- **id:** Unique team–season identifier number.  
- **team:** Name of the football club.  
- **country:** Country in which the club competes.  
- **league:** Name of the domestic league in which the club competes.  
- **season_start:** The starting year of the season.  
- **season_end:** The ending year of the season.  
- **home_w:** Number of matches won when playing at home.  
- **xg_h:** Average xG per match at home.  
- **pen_h:** Number of penalties awarded in favor of the club at home.  
- **Dataset Size:** The complete dataset is expected to contain ≈1281 rows and ≈49 columns after preprocessing.
## Expected Findings
* Home advantage is expected to have declined after VAR, with measurable decreases in performance indicators such as home-win rates, home points, and xG.
* Referee decisions such as penalties, fouls, and cards are likely to be more balanced between home and away teams.
* VAR may have reduced referee bias and the psychological effect of crowd pressure.
* The effects of VAR may be stronger in leagues where referee reliability is lower, such as the Turkish Süper Lig, compared to more reliable leagues like the Premier League or Bundesliga.
## Challenges, Future Work & Ethical Considerations
- Challenges: Some older seasons may have data gaps, and fully isolating VAR’s effect may be difficult due to other factors like crowd presence or the COVID-19 seasons.
- Future Work: Future research could include more leagues and additional metrics for a broader perspective.
- Ethical Considerations: All data sources and methods will be transparently documented. Ethical sensitivity will be maintained when interpreting results involving referee behavior.
