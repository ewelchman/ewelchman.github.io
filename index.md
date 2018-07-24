---
layout: default
---

# Recent Posts

* Nothing here yet.

# NFL analytics projects/posts


## Scraping and processing

* [**Scrape play-by-play from PFR**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/pbp_data_acquisition.ipynb).
A scraper to grab tables from pro-football-reference.com.

* [**Cleaning play-by-play data**].
Take play-by-play data scraped from PFR and parse the play details to determine play type and results.

* [**Scrape drive-level data from ESPN**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/espn_scraper.ipynb).
A scraper specific to ESPN's web interface to grab play-by-play data. I also process the detailed descriptions of individual plays to determine a play type (run/pass/punt, etc.) as well as the yardage gained.

* [**Scrape tables from PFR with Selenium**].
Use Selenium to work with pro-footbal-reference.com's javascript and (potentially) manipulate the page in a more sophisticated way.

## Modeling/Analysis

* [**Modeling win-percent**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/modeling_winpct.ipynb).
Given the game state, determine how likely one team is to go on to win the game. I try using logistic regression, a small neural net, and random forest algorithms as models and evaluate the performance of each.

* [**Model NFL games with Monte Carlo**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/montecarlo_games.ipynb).
Simulate football games by drawing from a pool past drives. I score each past drive by similarity to the current game state in order to determine whether to accept a candidate drive chosen randomly from the pool. I verify that a win probability estimate based on repeated simulations converges to a single value and compare the model's predictions to those of ELO ratings. Tests on a small sample set indicate performance comparable to or better than ELO ratings.

# Other data projects

* [**Investigating dropped packets**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/dropped_packets.ipynb). 
A fairly straightforward data exploration in order to investigate where and why some data packets were being dropped in the Wake Forest network.

* [**Scrabbledice**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/scrabbledice.ipynb).
Designing a Boggle-like set of dice for a board game: I implement a genetic-adjacent algorithm to find the best way to arrange letters on the dice, then for a sanity check I look at the results that score best.
