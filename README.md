# Data-Driven-Performance-Evalaution-and-Player-Ranking-in-Football-through-Machine-Learning

This repository showcases a machine learning project designed to evaluate and rank football players based on position-specific metrics. By using advanced algorithms, the project provides actionable insights to enhance decision-making for coaches, scouts, and analysts.


## Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Folder Structure](#folder-structure)
4. [Key Features](#key-features)
5. [Findings and Insights](#findings-and-insights)

---

## Introduction
This study explores how machine learning can enhance player evaluation and rankings by tailoring models to position-specific metrics. The project goes beyond traditional stats like goals and assists to provide deeper insights into player contributions.

---

## Objectives
1. Develop predictive models for position-specific performance metrics.
2. Create clustering algorithms for nuanced player rankings.
3. Identify impactful features using advanced feature selection methods.
4. Compare model predictions to existing player rankings for validation.

---

## Folder Structure
- **Player_Ranking**: predicted rating ranking  Clustering-based ranking algorithm with visualizations for each position.
- **Position_Specific_Target_Variable**: Scripts for preprocessing, feature selection, and modeling for each position.
- **Overall_Rating_Target_Variable**:Scripts for preprocessing, feature selection, and modeling for each position focused on overall player ratings.

---

## Key Features
- **Feature Selection**: Used Extra Trees Regressor, Mutual Information, and Select K-Best Regression to identify key metrics.
- **Models Applied**: XGBoost, Random Forest, Gradient Boosting, Adaboost Regression, Decision Tree Regression, Neural Networks, and Support Vector Regression.
- **Hyperparameter Tuning**: Optimized using Grid Search with cross-validation, leveraging different subsets of features to balance model complexity and performance.


---

## Findings and Insights

### Goalkeepers
- **Top Models:** Gradient Boosting and Voting Regressor achieved the best results, with R² scores of 0.776 on test data. Simpler models like KNN struggled to handle the dataset's complexity.
- **Key Features:** Saves (inside and outside the box), fouls, aerial duels lost, flow centrality, and dribbled past were critical for performance predictions.
- **Clustering Insights:**  
  - **Cluster 0:** Balanced performers excelling in consistency and defensive actions.  
  - **Cluster 1:** More aggressive and involved, contributing to chances and assists but prone to dangerous mistakes.

### Midfielders
- **Top Models:** Neural Networks and XGBoost performed best after tuning, balancing model complexity and accuracy with reduced features.
- **Key Features:** Ground duels won, key passes, fouls, shots blocked, and positional roles.
- **Clustering Insights:**  
  - **Cluster 0:** Versatile, contributing to both defense and offense.  
  - **Cluster 1:** Focused on offensive creativity through assists and key passes.  
  - **Cluster 2:** Defensive specialists excelling in ball recovery and aerial duels.

### Defenders
- **Top Models:** Support Vector Regression (SVR) and Gradient Boosting provided reliable predictions. Ensemble methods marginally improved performance.
- **Key Features:** Tackles, clearances, aerial duels, dangerous mistakes, and positional roles (e.g., full-backs, wing-backs).
- **Clustering Insights:**  
  - **Cluster 0:** Traditional central defenders excelling in key defensive metrics.  
  - **Cluster 1:** Aggressive full-backs with strong attacking contributions.  
  - **Cluster 2:** Balanced defenders without standout attributes.

### Forwards
- **Top Models:** XGBoost and ensemble methods (Voting and Stacking Regressors) performed best, with minimal overfitting after hyperparameter tuning.
- **Key Features:** Goals scored, assists, missed penalties, chances to score, and closeness centrality.
- **Clustering Insights:**  
  - **Cluster 0:** Goal-focused forwards excelling in finishing but with higher possession lost.  
  - **Cluster 1:** Creative forwards contributing to playmaking with assists, key passes, and accurate crosses.

### General Insights
- Ensemble methods consistently enhanced model stability and accuracy across all positions.
- Goalkeepers required fewer features for accurate predictions, while midfielders and forwards benefitted from a broader feature set.
- Defensive metrics were more challenging to predict due to the situational nature of actions.
- Clustering added value by grouping players based on similar strengths, aiding tactical decisions and player selection.




