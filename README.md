# Amex-default-prediction-
## Decribution
The objective of this competition is to predict the probability that a customer does not pay back their credit card balance amount in the future based on their monthly customer profile. The target binary variable is calculated by observing 18 months performance window after the latest credit card statement, and if the customer does not pay due amount in 120 days after their latest statement date it is considered a default event.
#### Model: neural network, 
#### Language used: python, spark rdd
#### Resource: google colab, google cloud dataproc, google storage
## Approach
#### data restructure
Each customer's data includes 18 months of bank statements, meaning there are 18 entries with the same customer_ID and target. To explore the statistics of a single customer's bank statements over these 18 months, I utilized the describe() method in a pandas dataframe. This method provides statistical values such as count, mean, standard deviation, minimum, 25th percentile, 50th percentile (median), 75th percentile, and maximum for each column in the dataset. so that the original of 190 columns expanded to 1504 columns, 18 entries for a single customer_ID and target combined to a unique entry by this way. 
#### training
I conducted an experiment to optimize the neural network architecture by adding 2, 3, and 4 layers, respectively. For each layer configuration, I used random search to find the optimal number of dense units for each layer and the best activation function. Specifically, I performed 100 trials for 2 layers, 200 trials for 3 layers, and 300 trials for 4 layers. Each trial was executed three times to ensure consistency and reliability of the results.
## Result
the highes sore in kaggle leaderboard is 0.80977, I got 0.76348. I am ranked 4170, in total of 6,003 competitors
##  Possible improvement
