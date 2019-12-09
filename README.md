# Kaggle-Challenge-Personalize-Expedia-Hotel-Searches-ICDM-2013
This is my challenge to do the Personalize Expedia Hotel Searches-ICDM 2013 of Kaggle 

The original website: https://www.kaggle.com/c/expedia-personalized-sort/overview?fbclid=IwAR2Fl7Auvx7T-J0ST6HF3aTXSPwJIHPuQ8NxPdX0Xbw8nfBBL7SFdKBz20g

## The Current method: RankNet
We were trying to create a pair-wise RankNet with two tensor inputs: **User Informations** and **Hotel Features**, both tensors will go through a dense neural network(we view it as a kind of convolution) and then concatenate them together, go through another dense neural network(we view it as calculating some kind of similarity between the two condensed tensors). Then we will make pairs of tensors and learn to rank them by the score which means the probability of the first one of the pair is prior to the second one. The accruacy will be evaluate by **NDCG**. 

### User Informations
### Hotel Features

## Future work
We would try to use more modern methods like list-wise learning to rank algorithms such as **LambdaRank** and **LambdaMART**.
