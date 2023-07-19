# PUBG_Game_Prediction
PlayerUnknown's Battlegrounds (PUBG) is a popular online multiplayer battle royale game. In a battle royale game, players fight to be the last person
or team standing. 
In order to win a PUBG game, it is important to have a combination of skill, strategy, and luck.
Now to predict the outcome of a game we need to train our model on a large dataset containing all various parameters of a game or information of a 
player like the guns he used, average headshot rate, his group rank etc. The datasets we are going to use 29 features. These 29 features along with 
the output of the game will be provided to train the model .

DATA INFORMATION : 
Data wrangling is the process of cleaning, organizing, and preparing data for analysis. In the context of the PUBG win prediction model, data wrangling would involve several steps to ensure that the data is in a usable form for the machine learning model.

Some of the data wrangling tasks that might be performed include:

Removing any unnecessary or irrelevant columns from the dataset

Handling missing values in the data (e.g. imputing missing values, dropping rows with missing values)

Converting categorical data, such as the type of equipment a player used, into numerical form (e.g. using one-hot encoding)

Splitting the data into training and testing sets

Performing these tasks is important because machine learning algorithms typically expect data to be in a specific format and can be sensitive to missing or incorrect values. By wrangling the data appropriately, we can ensure that the machine learning model is able to learn patterns in the data and make accurate predictions.

Now we can use this data for visualization as well which will help us get some insights about the game. 

![image](https://github.com/AnnuNITW/PUBG_Game_Prediction/assets/115100166/5848ed92-f079-46e0-8fe2-24174baddf14)

![image](https://github.com/AnnuNITW/PUBG_Game_Prediction/assets/115100166/c3b5feac-63e5-4248-8922-2280a0e03300)

![image](https://github.com/AnnuNITW/PUBG_Game_Prediction/assets/115100166/c6173d0a-2a6e-473a-8377-40700a687022)


![image](https://github.com/AnnuNITW/PUBG_Game_Prediction/assets/115100166/9b04bd49-82fe-4f2c-91fe-d3cf5d3d35b2)

![image](https://github.com/AnnuNITW/PUBG_Game_Prediction/assets/115100166/5ab13a1a-b777-4be2-958e-d0d23ffcf00b)

![image](https://github.com/AnnuNITW/PUBG_Game_Prediction/assets/115100166/2f5231ff-4dd5-48ba-adc7-e0d3a335f2ba)

These are just a few graphs that we can plot using the data. We can even perform EDA on this dataset. It all comes down to how creative you can be with the data. But for now, let’s focus on our new task i.e., Feature engineering.

FEATURE ENGINEERING : 
Feature engineering is the process of creating new features or modifying existing features in a dataset in order to improve the performance of a machine learning model. In the context of the PUBG win prediction model, feature engineering might involve creating new features based on existing data or transforming existing features in a way that makes them more useful for the model.

This might include normalizing the features.

Dropping unnecessary features which would only lead to increase in models complexity

Creating features based on combinations of existing features: For example, creating a new feature that represents the total number of kills a player made in a game, by summing up the number of kills made with each type of weapon.  

CATBOOST MODEL :
Let’s first take a look at why we chose the CatBoost Model for this dataset. 

CatBoost is effective for working with categorical data: The PUBG game includes a number of categorical features, such as the type of equipment a player used or the location on the map where a player was killed. CatBoost is particularly effective for handling categorical data, as it can automatically encode the categories as numerical values and handle missing values.

CatBoost is fast and easy to use: Training a CatBoost model is typically fast, and the library includes a number of built-in features that make it easy to use, such as automatic handling of missing values and support for parallelization. This can make it a good choice for quickly prototyping and testing models.

CatBoost is a powerful and accurate algorithm: In general, gradient boosting algorithms like CatBoost are known to be powerful and accurate, and they have been successful in a number of machine learning competitions. This makes them a good choice for many types of problems.

Given the characteristics of the PUBG game data and the strengths of the CatBoost algorithm, it is reasonable to consider using CatBoost for this type of problem.

After using CatBoost model for our dataset we can predict the performance using RMSE

![image](https://github.com/AnnuNITW/PUBG_Game_Prediction/assets/115100166/b98ddaf8-a23d-4eff-8f96-c183e51c8c81)

 
