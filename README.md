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
explore some algorithms. Forked repo can be found [here](https://github.com/faisal-samin/Data_Job_Analysis).

## Day 5 (21-09-21)

Another slip when building a streak... finding it more difficult to balance work, exercise, and now commuting to the office for the odd day in the week. 
But better to resume and try and build another (and hopefully longer) streak than give up altogether!

I've carried on working on the job classification repository and finalised the scraping code (and then ran the scraper which took a while) so we've now
got a freshly pulled job descripton data from indeed on 4 job classes. I realise there's been no ML over the past two days but that dataset is now 
ready to be exploited. Eager to look into this tomorrow!

## Day 6 (22-09-21)

Right, let's get the party started. The scraping took almost 2 hours last night but we now have a rich dataset with around 500 job adverts for 4 job titles in London, the majority of each have full, juicy descriptions. The goal is to train a multi-label classification model on this text using the job titles as labels.

A lot of the hard work to write the code for the sci-kit learn encoders and SVM model was already done for me but I did some exploration of the text with some word clouds to tailor the stop-words dictionary. A first model yielded an amazing 92.9% internal accuracy with a beautifully diagonal
confusion matrix. I looked into some mis-classified example to understand which words were swinging the model's decision but the ideal way of reviewing this
is through a visualisation - the code of which I need to refresh with my data. Full details can be found in the notebook at the repo [here](https://github.com/faisal-samin/Data_Job_Analysis/blob/master/analysis.ipynb).

Fun times with some learnings on how to evaluate a multi-label classification model.

P.S. Re-reading some of daily entries, I realise I'm often just rushing them with boring updates and lots of typos (thanks to a bash text editor) so I can head to bed on time. But I'll work on these to make them more interesting, maybe even review and flesh out more detail retrospectively.

## Day 7 (23-09-21)

Most of my interests during these 30 days seemed to be driven by work needs (which has its pros and cons!). Today, it's topic modelling which partially
falls into the realm of ML if we're being loose as it's an unsupervised method. I did a quick search on the topic and thought it would be useful to go
through Chapter 6 of the excellent tidy text book which is available online for free [here](https://www.tidytextmining.com/topicmodeling.html).

I went through about half of the Chapter and picked up some useful points already:
* Some of the general features of the Latest Dirichlent algorithm (LDA) and how it treats each document as a mixture (or a soup) of topic, and each topic as a mixture of words which is in constrast to some of the "hard clustering" algorithms with stricter dichotomies.
* How the beta values, i.e. the per-topic-per-word probabilities, can be studied to get a sense of the label for each topic.
* How the gamme values, i.e. the per-document-per-topic probabilities, can be studied to understand the dominant topic for each document (or in this case, AP news articles).

Code in the repo [here](https://github.com/faisal-samin/topic-modelling-r/blob/main/topic_modelling.R)

## Day 8 (06-10-21)

Well, this has been quite the failure! After an almost 2-week hiatus, I've finally found time and energy to dedicate some time to plodding on
with this. A myriad of work pressures, a slight cold and busy weekends with family have occuped my time, and I say all this to make me feel
better about myself, but honestly, you can always make time for things that are a priority for you (which this certainly is for me). 

Anyway, today I spent the evening exploring a house prices dataset I fashioned together (see Day 3 update) but this time in R to explore the 
tidymodels/keras APIs for Machine Learning. I've done most of my ML processing in scikit-learn so this was a good chance to get my hands dirty
with R's packages of choice here. 

I remember coming across a [free course](https://supervised-ml-course.netlify.app/) on supervised ML in R developed by Julia Silge so I followed 
along to the regression sections. I did some EDA and simple modelling with base R's lm() function. The plan is to move on to more advanced
techniques tomorrow. 

I'll update with a link to my repo tomorrow. 
