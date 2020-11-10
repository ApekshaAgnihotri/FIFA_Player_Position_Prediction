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
1. Sklearn Multi-label classifier

![sklearn-archi](https://user-images.githubusercontent.com/58865447/98627319-cd69d200-22c8-11eb-9a19-da5848a08eb1.png)

2. Ensemble Models classifier

![Ensemble-Archi](https://user-images.githubusercontent.com/58865447/98627413-0f931380-22c9-11eb-8caf-524dc6061eb5.png)


### Outputs
For test records, the model first recommends top three player suitable for a particular position. 

![output-1](https://user-images.githubusercontent.com/58865447/98627540-51bc5500-22c9-11eb-9da5-1a07a115e8a0.png)


### Model Performance
We identified that our class distribution is imbalanced, hence we selected F1-Score to evaluate our model's performance.

For multi-label classifiers, Random Forest performed the best with 82.65% F1-score.
![Screenshot from 2020-11-09 20-23-23](https://user-images.githubusercontent.com/58865447/98627800-e921a800-22c9-11eb-9759-c8634ff6359c.png)

For one-vs-all ensemble models, again Random Forest performed the best with 95.70% 
![Screenshot from 2020-11-09 20-24-35](https://user-images.githubusercontent.com/58865447/98627904-2d14ad00-22ca-11eb-80ae-84504fc11fd1.png)


## Model Tunining
We also captured model's behaviour while tuning it. Please find the results below

K-fold Validation Results
![Screenshot from 2020-11-09 20-23-36](https://user-images.githubusercontent.com/58865447/98627985-5b928800-22ca-11eb-80c5-b512f9e5c8c7.png)

Random Forest tuning
![Screenshot from 2020-11-09 20-30-51](https://user-images.githubusercontent.com/58865447/98628061-82e95500-22ca-11eb-9d8d-7bdf29afed2e.png)



