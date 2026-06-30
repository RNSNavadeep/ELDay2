# ELDay2
itanic Dataset — Exploratory Data Analysis (Post-Preprocessing)

This project performs statistical analysis and visualization on the cleaned and preprocessed Titanic dataset, uncovering patterns in passenger age, fare, and survival.


🧹 Preprocessing Recap

Before analysis, the raw data was prepared with:


Missing value imputation — Age (mean), Cabin & Embarked (most frequent)
Column removal — dropped Name, Ticket, Cabin
Encoding — Sex and Embarked converted via One-Hot Encoding
Outlier removal — rows with Z-score > 3 in Age and Fare filtered out



📈 Descriptive Statistics

Computed core summary statistics for the two key numeric features:

StatisticAgeFareMean✅ Calculated✅ CalculatedMedian✅ Calculated✅ CalculatedMode✅ Calculated✅ CalculatedStandard Deviation✅ Calculated✅ Calculated

These metrics give a quick sense of the central tendency and spread of passenger ages and ticket fares.


📊 Visualizations

1. Histograms


Age Histogram — shows the distribution of passenger ages
Fare Histogram — shows the distribution of ticket fares


2. Boxplots


Age Boxplot — visualizes spread and any remaining outliers
Fare Boxplot — highlights extreme values in ticket pricing


3. Pairplot

A seaborn.pairplot() to visualize pairwise relationships and distributions across all numeric features at once.

4. Correlation Heatmap

A seaborn.heatmap() of the correlation matrix to identify which features move together.


🔍 Key Insights


Age distribution: The majority of passengers were around 30 years old, indicating a predominantly middle-aged population aboard the Titanic.
Fare distribution: Most passengers paid fares in the 0–10 range, suggesting a large portion traveled in lower fare brackets.
Outliers: The Fare column contains significantly more high-value outliers compared to Age.
Correlations found:

Survived ↔ Fare
SibSp ↔ Parch
Fare ↔ SibSp



Survival pattern: Since Fare correlates well with Survived, it suggests that higher-fare (first-class) passengers had a better chance of survival.



🛠️ Libraries Used

LibraryPurposepandasData manipulationnumpyNumerical operationsmatplotlibHistograms & boxplotsseabornPairplot & correlation heatmapscipyZ-score outlier detectionscikit-learnImputation & encoding


✅ Conclusion

This analysis builds directly on the preprocessed dataset, turning clean data into actionable insights — revealing that passenger class (via Fare) was a strong indicator of survival on the Titanic.
