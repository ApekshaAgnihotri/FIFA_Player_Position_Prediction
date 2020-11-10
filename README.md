# Player_Position_Prediction 
## Problem Statement

The object of our project is:
1. Design a system that can determine what positions a soccer player can play at, so that if a substitute is needed for a certain position, the players who can play there are known. 

2. Explore multi-label classifiers in Sklearn package.

3. See how ensemble models can be used for multi-label classification problems

### Dataset
We use FIFA soccer video game dataset to simulate the problem for actual players. 
​ https://www.kaggle.com/stefanoleone992/fifa-20-complete-player-dataset#teams_and_leagues.csv

Total Records: 90k
No. of Features: 104 per record

### Classes
Gk_positioning ls cm rcm rm st lwb rs ldm lw cdm lf rdm cf rwb rf lb rw lcb lam cb cam rcb ram rb
We one hot encoded it to feed it to our models.

### Models
Since, one player can play from more than one position, we identified our problem statement as a Muli-label classification problem. We considered following algorithms:
1. Logistic Regression 
2. Random Forest

We explored Sklearn's multi-label classifiers as well as built our own one-vs-all ensemble models for this purpose. Architectures for both the approaches are shown below:


### Outputs


### Results


