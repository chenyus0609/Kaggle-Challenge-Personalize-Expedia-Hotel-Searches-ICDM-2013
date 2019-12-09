# Kaggle-Challenge-Personalize-Expedia-Hotel-Searches-ICDM-2013
This is my challenge to do the Personalize Expedia Hotel Searches-ICDM 2013 of Kaggle 

The original website: https://www.kaggle.com/c/expedia-personalized-sort/overview?fbclid=IwAR2Fl7Auvx7T-J0ST6HF3aTXSPwJIHPuQ8NxPdX0Xbw8nfBBL7SFdKBz20g

## The Current method: RankNet
We were trying to create a pair-wise RankNet with two tensor inputs: **User Informations** and **Hotel Features**, both tensors will go through a dense neural network(we view it as a kind of convolution) and then concatenate them together, go through another dense neural network(we view it as calculating some kind of similarity between the two condensed tensors). Then we will make pairs of tensors and learn to rank them by the score which means the probability of the first one of the pair is prior to the second one. The accruacy will be evaluate by **NDCG**. 

<a href="https://imgur.com/f2h3Ury"><img src="https://i.imgur.com/f2h3Ury.png" title="source: imgur.com" width="50%" height="50%" /></a>

### User Informations
- srch_id
- site_id
- visitor_location_country_id
- visitor_hist_starrating
- visitor_hist_adr_usd
- srch_destination_id
- srch_length_of_stay
- srch_adults_count'
- srch_children_count 
- srch_room_count
- srch_saturday_night_bool
- orig_destination_distance
  
### Hotel Features
- prop_country_id
- prop_id
- prop_starrating
- prop_review_score
- prop_brand_bool
- prop_location_score1
- prop_location_score2
- prop_log_historical_price
- price_usd
- promotion_flag
- srch_query_affinity_score

## Future work
We would try to use more modern methods like list-wise learning to rank algorithms such as **LambdaRank** and **LambdaMART**.
