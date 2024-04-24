
# SC1015 Mini Project
![](https://github.com/jwistired/SC1015-MiniProject/blob/main/other/cover.png)

## About
This is a mini project for SC1015 (Introduction to Data Science and Artificial Intelligence). 

As the video game market is very big, and as video game enthusiasts and computing students, we would like to explore and analyse what could contribute to the success of a video game. Our main focus will be on video games from the online marketplace Steam.

## Dataset Used

https://www.kaggle.com/datasets/mexwell/steamgames

## Problem Definition

1) Find out what types of video games are successful
2) Find out common themes/factors that make them successful
3) Are we able to simulate the success of these games based on some of these factors

## Exploratory Analysis

We decided to analyse and plot 4 main points - Price, Metacritic Score, Genre and Length of description against the number of estimated owners of the video games. We hope that these data can allow us to determine what could contribute to the success of a video game.

For our findings, price and length of description have a low correlation to the ownership numbers. Generally, a higher Metacritic Score translates to higher ownership numbers. Genres such as Action, Adventure and Indie games perform better.

## Machine Learning

(i) Decision Tree Classifier
As video games with a higher Metacritic score generally perform better, we would like to see if we can use the Metacritic score to predict if a video game would be successful. We will make use of a Decision Tree Classifier on our train-test split dataset to determine if a game is successful from the Metacritic Score. 

Overall, our model achieved a classification accuracy of around 0.77, with a True Negative Rate of 0.96 and a True Positive Rate of 0.2. False Positive Rate remains low at 0.03.

(ii) Recurrent Neural Network (New)
While we initially determined that the length of the description does not have much correlation to the success of a video game, we wanted to see if we could generate a description  of a video game based on other well-performing games of the same genre, similar to the Gen AI we have out there.

We filtered out the data for games that perform well, and made use of Recurrent Neural Network to train on our data set. Our model will take in the input with an embedding layer that maps the character ID to a vector. It also consists of 2 GRU layers for recurrent computation and a Dense output layer.

Using the model, we are able to generate text, character by character, by giving it an initial prompt.

In the future, further improvements to the model could be made by using a more specific dataset, applying regularisation and dropout or adding more layers and training on more epochs.
   
## Conclusion and Insights

### Conclusion
1) Initial findings on what factors could affect sales (game ownership)
2) Factors such as Metacritic Scores play a bigger part in game ownership
3) Able to use Metacritic Scores to predict success of a game
4) Able to utilise our data and RNN to assist with generating a game description

### Additional Insights
1) Generally, a shorter game description may result in lower ownership
2) Free games may also have higher ownership as they are more accessible
3) Niche genres such as "Web development" games perform poorly in general and should be avoided.

## Contributors
1) [@jwistired] (https://www.github.com/jwistired) - Jing Woon: Project Idea, Dataset Finding, Group Meeting coordinator, Presenter
2) [@jerrald-s] (https://www.github.com/jerrald-s) - Jerrald: Data preparation & cleaning, Exploratory analysis and data visualisation, application of Machine Learning on the dataset, research into Recurrent Neural Network and attempt of application to the project
4) [@whyzaac] (https://www.github.com/whyzaac) - Yi Jun: Facilitate in Project Ideation and Project Objectives, Dataset Finding, Presenter

## References
1) https://www.kaggle.com/datasets/mexwell/steamgames
2) https://www.tensorflow.org/text/tutorials/text_generation
