---
layout: default
---

# Blog posts

* [**Was week 7 a turning point for the Carolina Panthers?**](https://www.catscratchreader.com/2018/10/31/18038790/was-week-7-a-turning-point-carolina-panthers-baltimore-ravens-nfc-south)
A profile of the Carolina Panthers offense using stats from the first six weeks of the 2018 season.

# NFL analytics projects/posts


## Scraping and processing

* [**Scrape PFR**](https://github.com/ewelchman/scrape_pfr).
A github repo containing scripts that I use to scrape NFL data from <http://pro-football-reference.com>, as well as scripts to parse the raw tables and produce data files for further analysis. 
I have written descriptions of how previous iterations of some of the individual scripts work.

  * [**Scrape play-by-play from PFR**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/pbp_data_acquisition.ipynb).
A scraper to grab tables from pro-football-reference.com.

  * [**Scrape tables from PFR with Selenium**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/pfr_scraper_selenium.ipynb).
 Use Selenium to work with pro-footbal-reference.com's javascript and (potentially) manipulate the page in a more sophisticated way.

* [**Scrape drive-level data from ESPN**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/espn_scraper.ipynb).
A scraper specific to ESPN's web interface to grab play-by-play data. I also process the detailed descriptions of individual plays to determine a play type (run/pass/punt, etc.) as well as the yardage gained.

## Modeling/Analysis

* [**Modeling win-percent**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/modeling_winpct.ipynb).
Given the game state, determine how likely one team is to go on to win the game. I try using logistic regression, a small neural net, and random forest algorithms as models and evaluate the performance of each.

* [**Model NFL games with Monte Carlo**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/montecarlo_games.ipynb).
Simulate football games by drawing from a pool past drives. I score each past drive by similarity to the current game state in order to determine whether to accept a candidate drive chosen randomly from the pool. I verify that a win probability estimate based on repeated simulations converges to a single value and compare the model's predictions to those of ELO ratings. Tests on a small sample set indicate performance comparable to or better than ELO ratings.

* [**Modeling NFL player stats with an LSTM neural network**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/playerstats_lstm.ipynb). 
Use an LSTM neural network implemented in TensorFlow to predict individual player stats in NFL games. The dataset comes from scraping pro-football-reference.com; my code for scraping and parsing the data can be found on github. I use stats from 2013-2016 for training, and 2017-2018 for testing and validation. The model is a two-layer LSTM cell. I transform the data with a scaling function prior to feeding the model, and use a mean-squared error cost function with a little bit of L2 regularization to help prevent overfitting, with the Adam optimizer. I do this with two different scalers and show that the results differ wildly. Finally, I transform output back to recognizable data in order to visually compare predictions with reality.


* [**NFL game-flow sankey diagrams**](https://github.com/ewelchman/sankey_app).
A Flask web app that uses dash and plotly to create Sankey diagrams in order to visualize detailed play-by-play information and summarize offensive or defensive performance. The app takes raw play-by-play data to create a dynamic illustration of offensive performance. This kind of visual aid provides instant and intuitive understanding that can be difficult to illustrate with numbers alone.

# Other data projects

* [**Investigating dropped packets**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/dropped_packets.ipynb). 
A straightforward data exploration in order to investigate where and why some data packets were being dropped in the Wake Forest network.

* [**Scrabbledice**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/scrabbledice.ipynb).
Designing a Boggle-like set of dice for a board game: I implement a genetic-adjacent algorithm to find the best way to arrange letters on the dice, then for a sanity check I look at the results that score best.
