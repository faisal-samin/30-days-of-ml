# 30-days-of-ml
Repository to capture updates of a 30 day self-directed journey to learn and revise ML concepts. 

## Day 0 (13-09-21)
The goal throughout these 30 days is to develop and revise Machine Learning knowledge by spending at least an hour everyday on reading, studying and learning concepts. Some general rules:

- I will tweet and document progress on twitter and github for self accountability.
- Use a variety of resources such as notebooks, MOOCs, books and video tutorials.

Some minimum goals in mind:

- Tackle at least 3 Kaggle challenges
- Go over 5 chapters of HOML
- Go over 5 chapters of ISLR

## Day 1 (14-09-21)

Not a very successful start to the 30 days. Spent about an hour installing and configuring a new zsh shell (iTerm) to upgrade my terminal experience and feel like a pro.
However that led to issues when trying to launch a jupyter notebook. Currently trying to install this with brew but that's taking forever and doesn't appear to be working...

The plan was to go through the notebook for Chapter 2 of the excellent HOML (and the chapter itself is a super overview of the ML process from end to end) but the aforementioned 
distraction/bug cut into that. Better make up for this with some more study time tomorrow. 

Main takeaways today were the endless amount of configuration options for terminal shells, but also the advatanges of isolated environments for Python packages which I've got a (virtual) 
sticky note for. 

Hoping for progress tomorrow!

## Day 2 (15-09-21)

Right, so I managed to resolve the issue with jupyter and another packages; turns out it was to do with a major Mac OS upgrade which required a re-install of Command Line Tools. *shrugs*
Anyway, we're back in business.

Once again, Chapter 2 of this book is worth re-visiting again and again to refresh some core concepts of approaching any ML project. I followed along to the book and ran the accompanying
notebook (from the authors GitHub repo) alongside. Today is very much just reading and absorbing.

Some of the key takeaways from this chapter for me:
* The advantages of data pipelines with asynchronous components for ETL jobs, data processing, training models etc. If one components breaks, the rest of the system is unaffected.
* The importance of framing a Machine Learning problem and designing a system (e.g. supervised vs unsupervised, single/multiple regression, classification/regression, is batching required.
* The aforementioned benefits of using isolated environments to manage packages using virtualenv.
* Creating functions wherever you can to make life easier and work reproducible, even for small tasks like downloading datasets.
* Useful pandas methods such as .describe() and .info()
* The importance of visualisations like scatterplots (for relationships) and histograms (distributions). In the example for the Chapter 2, a capped field is spotted thanks to a histogram.
* Computing hashes of each instance's identifier to create stable train/test splits which will even function with updated datasets.

The beauty of scikit-learn's design is at great show towards the end of this Chapter. A note to self to re-read and adopt some of the coding principles here with my own ML project.

That's it for today - hoping to do some more coding tomorrow, maybe with an introductory Kaggle competition (in whatever I can do in an hour!). 

## Day 3 (16-09-21)

Had a fairly busy day so chugging along with the 30 days with a less demanding task today. For a work side-project, I've prepared a dataset on UK House Prices
for a Kaggle regression competition (similar to the classic Kaggle competition on the ames housing data). 

Before I set people loose on the dataset and building models, I first need to check the integrity of data and check whether any variables come out as significant
in predicting house prices.

I developed a notebook with steps for  elementary processing, cleaning and one-hot encoding before training a basic linear regression model with three variables (one
numerical and two categorical) and can be found [here](https://github.com/faisal-samin/uk-house-prices/blob/main/notebook_linreg_model.ipynb). The primary
goal was to check whether a basic model could be developed to a reasonable accuracy level and I managed to get a model with an R^2 value of 0.7 (assuming
that will be the main accuracy score) which is fairly reasonable without doing any feature engineering or exploring other models. 

Main takeaways:
* Consideration of the right accuracy metrics when designing a "Kaggle" competition to suit the needs of the modelling task. With a regression model, is R^2 
the best? 

## Day 4 (19-09-21)

Unfortunately, I've had to take an hiatus over the last two days (a busy Friday, then a Saturday with family), neither of which are real excuses to be fair. 
I'll try and keep the streak consistent through the next weekened! 

I was keen to dip my toes into a multiclass text classification project today, and this is partly related to a work need. To start off, I dug out this 
Medium [notebook](https://medium.com/analytics-vidhya/classifying-tech-data-job-postings-on-indeed-com-1fd8ca6e7cdd), forked the repo and went about
adapting the web-scraping code to scrape jobs ad in London for some tech/data positions. 

This was easier said than done however as the web-scraping code, which was written in 2018. no longer worked. Most of my evening was spent
re-writing the code in BeautifulSoup with the new div classes and span tags and there is still some work left to go to extract the full job text from
individual hyperlinks (which I've now gathered). Part 2 on this tomorrow when I'll hopefully get a chance to start playing around with the data and 
explore some algorithms.
