# Netflix User Behavior Analysis & Recommendation System

## Project Overview
This project analyzes user viewing behavior on a Netflix-like platform
and explores both churn prediction and recommendation systems
to understand user engagement and retention challenges.

## Dataset
This project uses a synthetic Netflix-like dataset
(Netflix 2025: User Behavior Dataset, 210K+ records)
provided for educational purposes.

The analysis is based on the following files:

| File | Rows | Description |
|------|------|-------------|
| users.csv | ~10K | User demographics and subscription information |
| movies.csv | ~1K | Movie and TV show metadata |
| watch_history.csv | ~105K | User viewing history with progress and timestamps |

## Exploratory Data Analysis (EDA)
Key findings:
- Majority of users have fewer than 10 interactions
- Strong long-tail distribution in content popularity
- High proportion of cold-start users

These characteristics strongly impact both churn modeling
and recommendation performance.

## Churn Prediction (Supporting Analysis)
- Goal: Identify behavioral patterns associated with user inactivity
- Features: watch frequency, completion rate, viewing diversity, recency
- Models explored: baseline classifiers / survival analysis
- Insight: Low engagement users show significantly higher churn risk

⚠️ This analysis is used to support behavioral understanding,
not as the primary deliverable.

## Recommendation System (Main Focus)
### Collaborative Filtering (ALS)
- Implicit feedback with weighted interactions
- Recall@10 ≈ 0.001 due to extreme data sparsity and limited user histories

### Content-Based & Cold-Start Strategy
- Movie metadata embedding
- More robust for users with few interactions
- Recall@10 ≈ 0.01, outperforming collaborative filtering under cold-start conditions

### Hybrid Approach
- Weighted combination of ALS and content-based scores
- Limited improvement due to structural data constraints

## Conclusion
This project highlights the practical limitations of recommender systems
under sparse and imbalanced user behavior data.
Rather than optimizing for raw performance, the focus was placed on
understanding data constraints, comparing model robustness,
and designing strategies suitable for real-world cold-start scenarios.

