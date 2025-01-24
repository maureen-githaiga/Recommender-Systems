# Recommender Systems Assignment

This repository contains the implementation of various recommender system techniques as part of the course assignments/projectwork.
The work includes collaborative filtering, group recommendations, sequential recommendations, and explanations for "why not" questions in group recommendations.

## Files

- **1_collaborative_filtering.ipynb**: Implements a user-based collaborative filtering approach for movie recommendations using the MovieLens 100K dataset.
- **2_group_recommendations.ipynb**: Implements two aggregation methods for group recommendations:
  1. **Average Method**: Aggregates ratings by averaging the scores of all group members.
  2. **Least Misery Method**: Aggregates ratings by selecting the minimum score given by any group member.
  Additionally, an extra method takes user disagreements into account when producing group recommendations.
- **3_sequential_recommendations.ipynb**: Implements a sequential recommendation system for group recommendations, taking into account the sequence of user preferences.
   The method allows for the evaluation of group recommendations across different sequences and rounds.
- **4_why_not_explanations.ipynb**: Implements methods for providing explanations on "why not" questions for group recommendations at various granularities. This includes explanations for matrix-based, group-based, and position absenteeism cases.

## Overview of Tasks

### 1. Collaborative Filtering
This section implements a collaborative filtering recommendation system using the MovieLens 100K dataset. The system recommends movies based on user ratings and similarities between users.

### 2. Group Recommendations
- **Part (a)**: We implemented two methods for aggregating recommendations for a group:
  - **Average Method**: Aggregates ratings by averaging the individual ratings across all group members.
  - **Least Misery Method**: Selects the minimum rating from any group member as the group's recommendation.
  
- **Part (b)**: A method was developed to handle disagreements among users in a group. This method identifies discrepancies between user preferences and adjusts the recommendations accordingly to reflect group dynamics.

### 3. Sequential Recommendations
- In this section, we designed and implemented a new method for sequential group recommendations, which takes into account the sequence in which items are recommended and interacted with. This approach is based on modifying existing methods to improve group recommendation quality by considering sequential preferences.
- We evaluated the top-10 recommendations for a group of 3 users, across 3 different recommendation sequences (i.e., 3 rounds) using the MovieLens 100K dataset.

### 4. Why Not Explanations
- **Granularity Cases**: The implementation of "Why Not" explanations for group recommendations is based on multiple granularity levels, including atomic and group-level cases. This helps explain why a particular item is not recommended.
  - **Atomic Case**: Explanations for why a particular item was not included in the recommendation list (e.g., "Why not Matrix?").
  - **Group Case**: Explanations for why an entire category or genre is not recommended (e.g., "Why not action movies?").
  - **Position Absenteeism Case**: Explanations for why an item was not ranked higher in the list (e.g., "Why not rank Matrix first?").
  
For each of these cases, explanations are provided for a group of 3 users and based on their top-10 recommendations.

