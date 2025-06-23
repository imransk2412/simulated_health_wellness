# simulated_health_wellness
# Tailoring Wellness Programs via Clustering

This project applies unsupervised machine learning techniques—K-Means and Agglomerative (Hierarchical) Clustering—to segment participants in a workplace wellness program based on key behavioral and health features. The aim is to design targeted and personalized wellness interventions that improve health outcomes, boost engagement, and reduce healthcare costs.

##  Dataset

The simulated dataset includes **500 participants** with the following features:
- `Exercise_Time_Min` – Average daily exercise time (minutes)
- `Healthy_Meals_Per_Day` – Count of healthy meals consumed daily
- `Sleep_Hours_Per_Night` – Average sleep duration (hours)
- `Stress_Level` – Stress level on a scale of 1 to 10
- `BMI` – Body Mass Index

All features were standardized using `StandardScaler`, and PCA (Principal Component Analysis) was applied to enhance cluster separability and reduce dimensionality.

##  Methods

Three clustering approaches were evaluated:
- **K-Means** (original features)
- **Agglomerative Clustering** (Hierarchical)
- **K-Means with PCA-transformed features**

###  Cluster Evaluation
- The **elbow method** was used to determine the optimal number of clusters.
- **Silhouette Scores** were calculated to measure cluster cohesion and separation.

##  Results

| Clustering Model       | Silhouette Score |
|------------------------|------------------|
| K-Means (original)     | 0.1516           |
| Hierarchical           | 0.1363           |
| K-Means on PCA         | **0.3626**       |

The best clustering was achieved with **K-Means using PCA**, producing **three well-separated clusters**:

### Cluster Profiles:
- **Cluster 1: Health-Minded** – High exercise, healthy diet, normal BMI, low stress
- **Cluster 2: At-Risk** – Low exercise, poor diet, high BMI, high stress
- **Cluster 3: Moderate** – Moderate habits, borderline BMI, slightly high stress

## 📉 Visualizations

- **Elbow Plot** – Optimal number of clusters = 3
- **Dendrogram** – Hierarchical groupings
- **PCA Scatterplot** – Clear cluster separation
- **Correlation Heatmap** – Stress positively correlated with BMI, while exercise was negatively correlated with BMI

##  Recommendations

- **Segment-Specific Content**: Design tailored programs for each behavioral group
- **Digital Nudges**: Use app notifications and wearables for real-time support
- **Re-Clustering**: Periodically reassess users to adapt interventions over time
- **Feedback Loop**: Collect user feedback to refine clustering strategies

##  Limitations

This study used simulated data. Real-world validation is necessary to confirm the clustering effectiveness across diverse demographics and clinical scenarios.

##  Conclusion

Clustering techniques, especially K-Means with PCA, enable meaningful segmentation of wellness program participants. Personalized interventions based on clustering insights can enhance relevance, engagement, and outcomes—supporting a shift from generalized wellness programs to **data-driven personalization**.

##  References

- Carolan, S., Harris, P. R., & Cavanagh, K. (2017). *Journal of Medical Internet Research*, 19(7), e271. [Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5550734/)
- Greiner, B. A., et al. (2022). *PLOS ONE*, 17(11), e0277114. [Link](https://pubmed.ncbi.nlm.nih.gov/36383613/)
- Munir, F., et al. (2015). *BMC Health Services Research*, 15(1), 1–11. [Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7267007/)
- Naylor, C. D., et al. (2018). *Health Affairs*, 35(5), 769–775. [Link](https://pubmed.ncbi.nlm.nih.gov/27140981/)
