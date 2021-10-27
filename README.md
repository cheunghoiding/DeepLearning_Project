# DeepLearning_Project
Neural Collaborative Filtering Recommendation System over MovieLens Dataset.

## Modern Days Recommender System
Widely used in majority of real-world domains, ranging from entertainment and ecommerce to even dating apps.

Why is high-quality recommender system important?
1. Personalised user experience
2. Build long-term trust and loyalty
<img width="551" alt="Screenshot 2021-10-27 at 9 44 42 AM" src="https://user-images.githubusercontent.com/84705479/138985822-19bce33b-fb16-4851-a722-5055ef6a2cd3.png">

Challenges in developing one:
- Time-consuming
- Cold Start Problem
- Customer Expectations
- Lack thereof Explicit Feedback

## Evolution of Recommender System Algorithms
<img width="1158" alt="Screenshot 2021-10-27 at 9 47 15 AM" src="https://user-images.githubusercontent.com/84705479/138986059-39e0404d-e111-4436-a26d-96b1d9b2f5c8.png">

## Embedding
<img width="1025" alt="Screenshot 2021-10-27 at 9 49 49 AM" src="https://user-images.githubusercontent.com/84705479/138986277-2b567feb-37d5-4d67-b6a2-35fd14fa7a6a.png">
<img width="986" alt="Screenshot 2021-10-27 at 9 50 13 AM" src="https://user-images.githubusercontent.com/84705479/138986318-5e49d94a-b29b-48aa-80ea-3c5ae08d14d1.png">
<img width="1107" alt="Screenshot 2021-10-27 at 9 50 27 AM" src="https://user-images.githubusercontent.com/84705479/138986322-b9ae9243-c54e-4423-9161-5eaef55dcf04.png">

## Explicit Feedback VS Implicit Feedback
<img width="967" alt="Screenshot 2021-10-27 at 9 51 14 AM" src="https://user-images.githubusercontent.com/84705479/138986377-14e0b6aa-da24-4775-a07c-c6961a275c37.png">
<img width="1025" alt="Screenshot 2021-10-27 at 9 51 23 AM" src="https://user-images.githubusercontent.com/84705479/138986383-f9014715-96c7-4667-a689-28082afd25e9.png">

## Leave-One-Out Test Data Sampling Method
<img width="1062" alt="Screenshot 2021-10-27 at 9 52 04 AM" src="https://user-images.githubusercontent.com/84705479/138986430-b5f3b5f7-886f-44f0-8cd2-7163b5616028.png">

## Neural Collaborative Filtering Model
<img width="918" alt="Screenshot 2021-10-27 at 9 52 26 AM" src="https://user-images.githubusercontent.com/84705479/138986472-e77a64d9-e644-4f58-840c-821da5581d8c.png">
<img width="792" alt="Screenshot 2021-10-27 at 9 53 25 AM" src="https://user-images.githubusercontent.com/84705479/138986556-2f53daa8-1b13-4d0d-a654-c8ac64a291ab.png">

- Change the target outcome from the rating to positive implicit feedback
- Add negative sampling

<img width="394" alt="Screenshot 2021-10-27 at 9 54 26 AM" src="https://user-images.githubusercontent.com/84705479/138986652-286d6ccd-2f31-4eb2-871c-b900a9c2f28c.png">
<img width="510" alt="Screenshot 2021-10-27 at 9 54 33 AM" src="https://user-images.githubusercontent.com/84705479/138986671-581fa28a-be0f-4b3c-8e86-435d4064f8fa.png">

- Using embedding and Neural Collaborative Filtering for deep learning
<img width="989" alt="Screenshot 2021-10-27 at 9 55 42 AM" src="https://user-images.githubusercontent.com/84705479/138986753-a9923f4b-569c-420b-8296-d18afe7b90e1.png">
<img width="1125" alt="Screenshot 2021-10-27 at 9 56 34 AM" src="https://user-images.githubusercontent.com/84705479/138986831-edf44aad-e97f-4a31-ae49-b07524a0fa28.png">

## Model Evaluation
- Some evaluation methods: 
  - Accuracy (Root Mean Squared Error (RMSE) ) – how accurately predict user opinions over items.
- For Recommendation System:
  - NOT interested in predicting the actual ratings of these movies in Recommendation System.
  - Interested in predicting that the user WILL INTERACT with these movies eventually.

### Hit Ratio @ 10
- Pick one recent item we know the user DID interact with; we call this item as our Target.
- We add 99 random samples and the Target to the pool.
- Use NCF model to find the probability in which the user WILL INTERACT with all 100 samples, and sort them - from highest to lowest - based on that probability.
- If the Target is properly placed among the Top 10 probabilities in which the user WILL INTERACT with, we get one hit rate.
- Repeat the same process for all 943 users, and see how many hit rates we can get out of the total.

<img width="1089" alt="Screenshot 2021-10-27 at 10 00 42 AM" src="https://user-images.githubusercontent.com/84705479/138987270-499da5a3-affe-4132-82e1-7a45602cbe41.png">

- 61.82% of users that are recommended the actual item, (among a list of 10 items) that they eventually interact with.

## Conclusion
What have we learned?
- Challenges and Difficulties in modern days recommender system.
- Think out of the box! Problem reformulation!.
- Different Neural Network Model.
- Importance of EMBEDDING in machine learning.
- Importance of LEAVE-ONE-OUT Technique.
- Different Evaluation Metrics.
