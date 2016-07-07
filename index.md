---
title       : Next Word Prediction using NLP
subtitle    : Building a next word predictor using Natural Language Processing Techniques
author      : Telvis Calhoun
job         : technicalelvis.com
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      #
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Goals

- Build a language model using blog, news and twitter text provided by [Data Science Capstone Course](https://www.coursera.org/learn/data-science-project/home/welcome).
- Use this language model to predict the next word as a user types - similar to the [Swiftkey text messaging app](https://swiftkey.com/en) 
- Create a word predictor demo using [R and Shiny](http://shiny.rstudio.com/).

--- .class #id

## Word Prediction using N-Grams
Assume the frequency count of "data" is 198, "data entry" is 12 and "data streams" is 10. We calculate the [maximum likelihood estimate](https://en.wikipedia.org/wiki/Maximum_likelihood) (MLE) as:

$$
P_{mle}(gram_{N}|gram_{N-1}) = \frac{frequency(gram_{N})}{frequenc(gram_{N-1})}
$$

The probability of "data entry" is:

$$
P_{mle}(entry|data) = \frac{12}{198} = 0.06 = 6\%
$$

The probability of "data streams" is:
$$
P_{mle}(streams|data) = \frac{10}{198} = 0.05 = 5\%
$$

If the user types, "data", the model predicts that "entry" is the most likely next word.

--- .class #id


## Model Performance

TODO... Show TDR vs coverage curve


--- .class #id


## Demo Application

- [Click here to try the Shiny App that demonstrates the recommender!](https://technicalelvis.shinyapps.io/prince_song_recommender/)

TODO: Screenshot

TODO...