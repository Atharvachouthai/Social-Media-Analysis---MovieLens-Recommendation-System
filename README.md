# Social-Media-Analysis---MovieLens-Recommendation-System



Project Overview

The goal of this project is to build a personalized movie recommendation system using the MovieLens ml-25m dataset. By leveraging network analysis, topic modeling, and collaborative filtering, this project provides a robust framework for recommending movies to users based on their tagging behaviors and rating patterns. The approach combines network and machine learning methods to capture the nuanced relationships within the movie-tag network, enhancing the recommendation system's relevance and adaptability to user preferences.

Dataset

The dataset used is MovieLens ml-25m, a rich source of user ratings and tags applied to movies. It includes:

  1. Nodes: Representing users and movies, totaling 56,678.
  2. Edges: Interactions like ratings or tagging, totaling 305,353.

Objectives
The main objectives of this project are:

  1. User and Community Detection: Identifying influential users or communities based on tagging behaviors to enhance personalization.
  2. Network Analysis: Exploring network properties like centrality and modularity for insights into the structure and dynamics of movie-tag interactions.
  3. Link Prediction: Applying link prediction metrics to discover hidden connections in the network and improve recommendation accuracy.
  4. Movie Recommendation System: Developing a collaborative filtering recommendation engine using KNN and Pearson correlation.

Methodology

  1. Data Preprocessing: A down-sampling approach reduced <img width="455" alt="Screenshot 2024-10-27 at 5 13 19 PM" src="https://github.com/user-attachments/assets/d960c7f1-a45b-466f-932a-7b8ce47fc95b">
the network to a manageable subset of 6,490 nodes and 21,213 edges.

  2. Community Detection:

      Algorithm: Louvain method was used for hierarchical community detection.
      Levels: Generated three levels of communities, with a final modularity score of 0.377 at the highest level, indicating well-defined user interests and genre groupings.
  
  3. Link Prediction:

      Using metrics like the Jaccard Index and Resource Allocation Index, the analysis revealed user pairs with similar movie tastes, pointing to potential niche recommendations.

  4. Topic Modeling:

      LDA: Applied to reveal four major themes: War/Film Noir, Family Fantasy, Drama/Comedy, and Thriller/Action. This provides thematic insights that complement genre-based recommendations.
     
  5. Collaborative Filtering for Recommendation:

      a. KNNBasic Algorithm: Implemented using Surprise library, with Pearson correlation as the similarity measure.
     
      b. Recommendation Generation: Predicts ratings for unviewed movies, filtering out already rated movies to suggest fresh recommendations.

  6. Results
     
      Evaluation:

        a.  Root Mean Square Error (RMSE): The model achieved an RMSE of 0.6608, indicating strong predictive accuracy for rating predictions on a scale of 1 to 5.
     
        b. Test RMSE: Consistent performance on the test set with an RMSE of 0.661, confirming the model’s reliability on unseen data.

  7. Conclusion
        This project effectively combines network analysis, topic modeling, and collaborative filtering to enhance movie recommendations. The system can dynamically adapt to user     preferences and offer tailored suggestions, improving user experience. Future improvements could involve refining community detection and incorporating more advanced link prediction techniques to capture latent user interests further.

