---
layout: default
---

# Recent Posts

* Nothing here yet.

# NFL analytics projects/posts


## Scraping

* [**Scrape play-by-play from PFR**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/pbp_data_acquisition.ipynb).
A scraper to grab tables from pro-football-reference.com.

* [**Scrape drive-level data from ESPN**].
A scraper specific to ESPN's web interface to grab play-by-play data.

* [**Scrape tables from PFR with Selenium**].
Use Selenium to gatecrash pro-footbal-reference.com's javascript and (potentially) manipulate the page in a more sophisticated manner.

## Modeling/Analysis

* [**Cleaning play-by-play data**].
Take play-by-play data scraped from PFR and parse the play details to determine play type and results.

* [**Modeling win-percent**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/modeling_winpct.ipynb).
Given the game state, determine how likely one team is to go on to win the game. I try using logistic regression, a small neural net, and random forest algorithms as models and evaluate the performance of each.

* [**Model NFL games with Monte Carlo**].
Simulate football games by drawing from a pool of a team's past drives. I score each past drive by similarity to the current game state.

# Other data projects

* [**Investigating dropped packets**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/dropped_packets.ipynb). 
A fairly straightforward data exploration in order to investigate where some data packets were being dropped in the Wake Forest network.

* [**Scrabbledice**](https://nbviewer.jupyter.org/url/ewelchman.github.io/projects/scrabbledice.ipynb).
Designing a Boggle-like set of dice for a board game: I implement a genetic-adjacent algorithm to find the best way to arrange letters on the dice, then for a sanity check I look at the results that score best.