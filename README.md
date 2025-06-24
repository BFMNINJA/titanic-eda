# Titanic Dataset Exploratory Data Analysis (EDA)

This project performs an exploratory data analysis (EDA) on the Titanic dataset to uncover key patterns, trends, and relationships that influenced passenger survival.

## Project Structure

- **task2.py**: Main script for data cleaning, analysis, and visualization.
- **Titanic-Dataset.csv**: The dataset used for analysis.
- **plots/**: Directory containing generated histograms, boxplots, correlation matrix, and pairplot images.
- **EDA_Inferences.md**: Markdown file summarizing key findings and inferences from the analysis.

## Steps Performed

1. **Data Loading & Cleaning**
    - Loaded the Titanic dataset using pandas.
    - Filled missing values in the 'Age' column with the median age.
    - Filled missing values in the 'Embarked' column with the most common port.
    - Dropped the 'Cabin' column due to excessive missing data.

2. **Summary Statistics**
    - Generated summary statistics (mean, median, standard deviation, etc.) for numeric features.
    - Displayed data info to check for missing values and data types.

3. **Visualization**
    - Created histograms and boxplots for numeric features (`Age`, `Fare`, `Pclass`, `SibSp`, `Parch`).
    - Generated a correlation matrix heatmap to visualize relationships between features.
    - Produced a pairplot to explore feature relationships and survival patterns.

4. **Insights & Inferences**
    - Documented key findings in `EDA_Inferences.md`, including:
        - Socio-economic status (class and fare) was a major factor in survival.
        - Most passengers were in 3rd class and paid low fares.
        - Outliers in fare and age distributions.
        - Patterns suggesting women and children were prioritized for survival.

## How to Run

1. **Set up a virtual environment (recommended):**
    ```sh
    python -m venv venv
    .\venv\Scripts\activate  # On Windows
    ```

2. **Install dependencies:**
    ```sh
    pip install pandas matplotlib seaborn
    ```

3. **Run the analysis:**
    ```sh
    python task2.py
    ```

4. **View Results:**
    - Check the `plots/` directory for visualizations.
    - Read `EDA_Inferences.md` for a summary of findings.

## Requirements

- Python 3.7+
- pandas
- matplotlib
- seaborn

## License

This project is for educational purposes.
