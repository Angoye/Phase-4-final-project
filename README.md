# Phase-4-final-project

**Title: Movie Recommendation System**

**Project Overview**

The primary business objective is to improve user engagement by providing personalized movie recommendations. By leveraging collaborative filtering techniques, we can predict a user's preference for a movie they have not yet rated. This approach is beneficial for streaming platforms and online movie databases, helping them suggest content that aligns with individual tastes.

**Data Information** 

The dataset used in this project consists of movie ratings provided by users. It includes key attributes such as userId, movieId, rating, timestamp, title, and genres. This dataset is well-suited for building a recommendation system because it captures explicit user preferences (ratings) along with metadata about the movies, such as their titles and genres.
The dataset is structured and sufficiently large to support machine learning models. It allows for the application of collaborative filtering, a widely used technique that utilizes user behavior patterns to generate recommendations. The presence of multiple ratings from different users ensures that the model can learn and make accurate predictions.

**Data Preparation**

To ensure high-quality recommendations, the following preprocessing steps were implemented:

Data Cleaning: Removed missing values and duplicate entries to maintain data integrity.

Merging Datasets: Integrated movie metadata with user ratings to enrich the data for better insights.

Normalization: Standardized rating values to enhance model performance.

Capping Ratings: Since predicted ratings could exceed the maximum allowed score (5), values were capped at 5 to maintain realistic recommendations.

**Methodology**

Model Selection: We selected ALS in PySpark as the best model after comparing it to other models such a user-based or item-based recommendations that were tested.

Hyperparameter Tuning: parameters like rank, iterations, and regularization were optimized.

**Model Performance**

The ALS (Alternating Least Squares) model in PySpark was used for generating movie recommendations. This model is well-suited for collaborative filtering problems and efficiently handles large datasets by leveraging matrix factorization.

**Model Evaluation:**

The model was evaluated using Root Mean Squared Error (RMSE), a common metric for recommendation systems.

The final RMSE achieved was lower than other tested models, indicating better predictive accuracy.

Compared to other approaches, ALS in PySpark provided the most reliable recommendations with reasonable computational efficiency.

**Recommendation of Best Model:**

ALS with Hyperparameter Tuning performed the best among tested models.

Tuning parameters such as rank, maxIter, and regParam improved performance significantly.

**Results & Findings**

Compared to simpler user-based or item-based collaborative filtering, ALS produced more accurate and personalized recommendations.

The optimized ALS model is recommended for deployment due to its superior balance of accuracy, scalability, and efficiency in handling large-scale movie recommendation tasks.

**How to Run the Project**

Install dependencies (pyspark, pandas, numpy, etc.).
Load the dataset into the notebook.
Run the preprocessing steps.
Train the ALS model.
Generate recommendations and evaluate the results.

**Future Improvements**

Adding content-based filtering (e.g., recommending movies based on genres).
Incorporating deep learning for better user preference prediction.
Deploying the model as a web application.

