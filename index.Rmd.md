<style>
.reveal h1, .reveal h2, .reveal h3 {
  font-weight: bold;
  color: black;
}
</style>


<style>
.reveal p {
    color: black;
}
</style>


Predicting Text App
========================================================
author: Maximiliano
date: 28/11/2020
autosize: true

About the app
========================================================
<br>
<strong style="color:red"> The app was created with an interactive spirit in order to minimize the time users spend typing.</strong> <span style="color:red">We trust in our algorithm so one of our features is to predict not only 1 but 3 words ahead of what the users have written. </span>

*Regarding the process of developing the app*, we took a corpus, analyzed its tokens, constructed n-grams, modeled probabilities and kept searching ways of improving it. 

<br>
<strong style="color:black"> Link to the app: </strong> [https://arg-maximiliano.shinyapps.io/PredictingTextApp/](https://arg-maximiliano.shinyapps.io/PredictingTextApp/)


About the algorithm
========================================================
<br>
<span style="color:blue"> We took the constructed n-grams and modeled probabilities with a <strong style="color:blue"> Kneser-Ney smoothing </strong> method to make predictions on the following words a user would want to type. </span>

- The higher order n-gram is a <strong style="color:black"> trigram </strong> in our algorithm.
- It first looks a match in trigrams, then searches in bigrams and finally it moves on to unigrams.
- At unigrams level, the algorithm takes top 10 frequent unigrams and to select suggestions for following words it takes the more frequent unigrams in the top 10 that are not the same as the previous two words the user has written.


How the app works?
========================================================
<strong style="color:green"> Steps required by the user: </strong>

1. <strong style="color:black"> Type </strong> a word or some words, as you prefer, in the text bar.
2. See the <strong style="color:black"> options </strong> we recommend you to save time typing.
3. <strong style="color:black"> Check the boxes </strong> if you find a good sugestion, the option selected will appear now right next to what you have written.
4. <strong style="color:black"> If not, keep writing </strong> and new suggestions will appear.

<strong style="color:green"> How are the options arranged? </strong>

The first word suggested is the top word our algorithm consider you will want to type next. Below you will find top 2 and 3 recommendations. At the bottom we allow us to propose you not 1 but 3 more words to follow what you have written.


Screenshot of the app
========================================================
<img src="./appScreenshot.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" width="50%" style="display: block; margin: auto;" />

<strong style="color:blue"> "How to use?" </strong> <span style="color:blue"> section on the second tab of the app provides further information of the app to the users such as *what steps are expected from them, how the suggested words are arranged and an idea of how the algorithm was developed.* </span>

