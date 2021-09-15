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

# Day 2 (15-09-21)

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

