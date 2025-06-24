
# Titanic Dataset: Inferences from EDA

## 1. Summary Statistics & Initial Observations
- **Age**: The mean age is around 29-30 years. The data was missing some age values, which have been filled with the median age.
- **Fare**: The fare distribution is highly skewed to the right (as seen in the histogram and the large difference between the mean and median/75th percentile), with a few passengers paying a very high fare.
- **Pclass**: Most passengers were in 3rd class.
- **Survived**: About 38% of the passengers in this dataset survived.

## 2. Inferences from Visualizations

### Histograms and Boxplots
- **Age**: The age distribution is somewhat normal, centered around 30. There are very few elderly passengers.
- **Fare**: The vast majority of passengers paid a low fare. The boxplot shows many outliers on the higher end, indicating a few wealthy passengers.
- **Pclass**: This is a categorical feature, but represented numerically. The histogram shows the distribution across the three classes, with 3rd class being the most populated.

### Correlation Matrix
- **Pclass & Fare**: There is a strong negative correlation between Pclass and Fare (-0.55). This is expected, as 1st class (lower number) has higher fares.
- **Pclass & Survived**: There is a negative correlation between Pclass and Survived (-0.34). This suggests that passengers in higher classes (lower Pclass number) had a higher chance of survival.
- **Fare & Survived**: There is a positive correlation between Fare and Survived (0.26). Passengers who paid higher fares were more likely to survive.
- **SibSp & Parch**: There is some positive correlation between the number of siblings/spouses and parents/children. This is logical as families would travel together.

### Pairplot
- The pairplot reinforces the observations from the correlation matrix.
- When looking at the distributions with `hue='Survived'`:
    - **Age**: The survival distribution across different ages seems quite similar, although it appears that very young children had a slightly higher survival rate.
    - **Fare**: Passengers who paid higher fares have a visibly higher survival rate.
    - **Pclass**: The survival rate decreases significantly from 1st to 2nd to 3rd class.

## 3. Patterns, Trends, and Anomalies
- **Trend**: Socio-economic status (proxied by Pclass and Fare) was a major factor in survival. Wealthier passengers in 1st class had a much higher chance of survival.
- **Pattern**: Women and children appear to have been prioritized during the evacuation. This can be explored further by creating specific plots for Sex vs. Survived.
- **Anomaly**: The maximum fare is very high compared to the mean, indicating a few extremely wealthy individuals on board. This is a significant outlier.

This concludes the initial EDA based on the provided hints. Further analysis could involve creating more detailed plots (e.g., survival rates by Sex, Embarked port) and feature engineering.
