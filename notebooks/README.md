# Notebooks Guide

This folder contains the complete analytical workflow for the
Netflix-style user behavior analysis project.

## Notebook Overview

### 01_eda_user_behavior.ipynb
Exploratory analysis of user interactions and feature engineering
for churn prediction and recommendation models.

### 02_churn_prediction_survival.ipynb
Supporting analysis using survival models to understand
behavioral patterns associated with churn.

### 03_recommender_als.ipynb
Collaborative filtering recommender system using implicit
ALS under highly sparse interaction data.

### 04_recommender_content_coldstart.ipynb
Content-based recommendation system with cold-start
handling using look-alike user profiles.

## Execution Order
Run notebooks in numerical order. Notebooks 03 and 04
assume preprocessed data from Notebook 01.

## Notes
Low offline recommendation metrics are expected due to
extreme data sparsity and limited user interactions.

