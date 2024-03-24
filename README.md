
## **Authors;** Vivian Maiyo, Josephine Wanjiru, Shalom Irungu, Brian Kanyotu, Stella Ndegwa, and Diana Mbuvi
## Project Overview
### Problem Statement
MovieLens is a web-based recommender system that proposes movies to its users. It is faced with the task of improving its services by proposing movies that suit their users' preferences. We focus on helping MovieLens by creating predictive models for recommending movies to users based on their taste in terms of genres and based on the best-rated movies. 


#### Objectives
* To **Generate accurate movie recommendations for each user.**
* To **Enhance user engagement and satisfaction by providing tailored movie suggestions that align with their preferences.**
* To **create a recommendation system that utilizes collaborative filtering to analyze user ratings.**
## Data
The data was sourced from MovieLens, and has been merged to have a total of 100836 rows and 6 columns.
## Data Preparation
We prepared the data by merging datasets, getting its statistical summary, checked for duplicated and null values.
## Exploratory Data Analysis
We did visualization using plots to understand the genre distribution, rating frequency, and that of highly and lowly rated movies.
![2024-03-24 (1)](https://github.com/shalomirungu/phase4_project/assets/149403427/d09ccd9b-e3c5-4f6b-a49e-be52606a9bbd)
![2024-03-24](https://github.com/shalomirungu/phase4_project/assets/149403427/266ea017-d88c-46d5-96f4-cf7f39be2b14)
## Univariate Data Analysis
We performed univariate data analysis to understand the distribution of individual features in the dataset. 
#### Data Splitting
We split the data into training and testing datasets, then  pivoted the ratings into movie features.
## Modelling
We performed the following models:

 **1. Memory-based Collaborative Filtering**
* **user-based collaborative filtering**
* **item-based collaborative filtering**
  
 **2. Model-based Collaborative Filtering**
* **surprise package(singular value decomposition)**
* **K nearest neighbors**
## Evaluation
We evaluated the performances of the above models by using their RMSE and MAE scores.The lower the MAE and the RMSE scores, the better performing the model is. 
## Modelling Results
 **user-based collaborative filtering**:
 We checked for user to user similarity using cosine similarity, with the value 0 being least similar and 1 being most similar. The RMSE and MAE for this model were 1.555 and 1.2026 respectively. For the memory-based filtering, this had the lowest MAE and RMSE, hence being the best performing model.
 
 **item-based collaborative filtering**:
The data was first normalized using MinMaxScaler, and the RMSE for this model was 2.5194 and the MAE is 2.2235

 **surprise package(singular value decomposition)**:
 The RMSE and MAE for this model is 0.8821 and 0.4973 respectively. 
 
 **K nearest neighbors**:
 Its RMSE and MAE were 0.4120 and 0.1572. GridSearch hyperparameter tuning was applied, and these scores remained the same. For the model-based filtering, this had the lowest RMSE and MAE hence the better performing model.   
 
 ## Conclusion and Recommendations
 User-based collaborative filtering outperforms item-based collaborative filtering in terms of both MAE and RMSE. KNN significantly outperform memory-based collaborative filtering methods in terms of MAE and RMSE. Among the two, KNN has the lowest MAE and RMSE, indicating that it is the better-performing model for this dataset.
 1. The recommendation system should be thoroughly worked on to boost accuracy inorder to maintain users' trust and engagement.
 2. KNN and SVD collaborative filtering should be used and frequently updated to enhance the system performance.
 3. The recommendation system should be regularly updated for new user ratings and movie data to improve relevance of the movies recommended to different users. 
## Necessary Links
* **Jupyter Notebook** [Notebook](Phase4_Project.ipynb)
* **Presentation** [Powerpoint Presentation]()
