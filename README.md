# Machine Learning

A collection of practical assignments in Machine Learning, covering data analysis, preprocessing, regression, classification, text processing, and ensemble learning using Python.

**Repository:** [Richeey01/Machine_Learning](https://github.com/Richeey01/Machine_Learning)

## About the Project

This repository contains practical assignments completed as part of a Machine Learning course. Each practical focuses on a particular stage of the machine learning workflow, from exploring datasets to training, evaluating, and comparing models.

The project uses Python, pandas, NumPy, Matplotlib, Seaborn, and scikit-learn. Jupyter Notebooks are used to organize the code, visualizations, explanations, and results.

### Main objectives

- Understand and explore datasets.
- Perform exploratory data analysis (EDA).
- Clean and preprocess data.
- Analyze correlations between features.
- Build regression and classification models.
- Apply text vectorization techniques.
- Evaluate model performance using appropriate metrics.
- Compare algorithms and analyze feature importance.
- Build reproducible machine learning pipelines.

## Project Structure

```text
Machine_Learning/
│
├── data/
│   └── abalone.data.csv
│
├── notebooks/
│   ├── practical_1_*.ipynb
│   ├── practical_2_*.ipynb
│   ├── practical_3_*.ipynb
│   ├── practical_4_*.ipynb
│   ├── practical_5_*.ipynb
│   ├── practical_6_text_classification.ipynb
│   └── practical_7_random_forest.ipynb
│
├── README.md
└── requirements.txt
```

*Note: The structure above is a project overview. Replace the wildcard notebook names with the actual filenames in your repository. The `requirements.txt` file is optional if you have not created it yet.*

### Directory description

| Path | Purpose |
|---|---|
| `data/` | Datasets used for experiments and practical assignments. |
| `notebooks/` | Jupyter Notebooks containing code, explanations, visualizations, and model evaluations. |
| `README.md` | Main documentation for the repository. |
| `requirements.txt` | List of Python dependencies required to run the project. |

## Practical Assignments

### Practical 1 — Data Exploration

Introduction to the dataset and its structure.

- Load and inspect the dataset.
- Examine the number of rows, columns, and data types.
- Identify missing values and potential data quality issues.
- Calculate basic descriptive statistics.

### Practical 2 — Exploratory Data Analysis

Analyze the Abalone dataset and relationships between numerical features.

- Explore feature distributions.
- Calculate correlations between variables.
- Create visualizations to identify relationships.
- Investigate highly correlated features.

**Dataset:** `abalone.data.csv`

### Practical 3 — Data Preprocessing

Prepare data for machine learning models.

- Separate features and the target variable.
- Split data into training and testing sets.
- Apply preprocessing using `ColumnTransformer` and pipelines where appropriate.
- Avoid data leakage by fitting preprocessing steps only on training data.

### Practical 4 — Regression

Train regression models to predict the number of rings in abalones.

**Target variable:** `Rings`

- Build a baseline regression model.
- Evaluate performance using MAE, RMSE, and R².
- Investigate multicollinearity using Variance Inflation Factor (VIF).
- Compare feature sets and analyze their impact on performance.

### Practical 5 — Classification

Explore classification techniques and evaluate their performance.

- Train a classification model.
- Analyze the confusion matrix.
- Calculate precision, recall, and F1-score.
- Evaluate ROC-AUC where appropriate.
- Investigate classification thresholds and the trade-off between false positives and false negatives.

### Practical 6 — Text Classification

Build a text classification model for Russian-language reviews labeled as positive or negative.

**Notebook:** `practical_6_text_classification.ipynb`

- Prepare a text dataset.
- Clean and normalize text.
- Convert text into numerical features using TF-IDF.
- Train a Multinomial Naive Bayes classifier.
- Evaluate accuracy and F1-score.
- Inspect incorrectly classified examples.

This practical demonstrates how machine learning models can classify text using numerical representations of words.

### Practical 7 — Random Forest

Train and compare tree-based regression models using the Abalone dataset.

**Notebook:** `practical_7_random_forest.ipynb`

- Build a Decision Tree baseline.
- Train a Random Forest Regressor.
- Compare model performance using MAE, RMSE, and R².
- Experiment with model hyperparameters.
- Analyze feature importance.
- Investigate how ensemble learning can improve prediction stability.

**Main task:** Predict the number of rings in abalones based on their physical measurements.

## Datasets

### Abalone Dataset

**File:** `data/abalone.data.csv`

The Abalone dataset contains physical measurements of abalones and their age-related ring counts.

Typical features include:

| Feature | Description |
|---|---|
| `Sex` / `gender` | Categorical sex indicator; the exact column name depends on the dataset version. |
| `Length` | Length of the abalone. |
| `Diameter` | Diameter of the abalone. |
| `Height` | Height of the abalone. |
| `Whole weight` | Total weight. |
| `Shucked weight` | Weight of the shucked meat. |
| `Viscera weight` | Weight of the viscera. |
| `Shell weight` | Weight of the shell. |
| `Rings` | Number of rings, used as a target in regression tasks. |

The original dataset contains 4,177 observations. Verify that your local CSV has the expected number of rows and that its column names match those used in your notebooks.

### Text Classification Dataset

Practical 6 uses a small educational dataset of Russian-language reviews with two labels:

- `positive` — positive review.
- `negative` — negative review.

The dataset is used to demonstrate text preprocessing, TF-IDF vectorization, and Naive Bayes classification.

## Technologies

- **Python** — programming language.
- **Jupyter Notebook** — interactive development and documentation.
- **pandas** — data manipulation and analysis.
- **NumPy** — numerical operations.
- **Matplotlib** and **Seaborn** — data visualization.
- **scikit-learn** — preprocessing, machine learning algorithms, pipelines, and evaluation metrics.

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Richeey01/Machine_Learning.git
cd Machine_Learning
```

### 2. Create a virtual environment

Windows:

```powershell
python -m venv .venv
.venv\Scripts\activate
```

Linux or macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

If `requirements.txt` exists:

```bash
python -m pip install -r requirements.txt
```

Otherwise, install the main packages:

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the `notebooks/` directory and select the practical assignment you want to run.

**Important:** Check the dataset paths inside each notebook. Relative paths should be configured consistently with the repository structure.

## Evaluation Metrics

The project uses several metrics depending on the task.

| Metric | Purpose |
|---|---|
| MAE | Average absolute prediction error. |
| RMSE | Prediction error that penalizes large errors more strongly. |
| R² | Measures how well a regression model explains variation in the target. |
| Accuracy | Proportion of correctly classified observations. |
| Precision | Proportion of predicted positives that are actually positive. |
| Recall | Proportion of actual positives correctly identified. |
| F1-score | Harmonic mean of precision and recall. |
| ROC-AUC | Measures the ability of a binary classifier to distinguish between classes. |

Not every metric is applicable to every assignment. Regression and classification metrics should be selected according to the problem being solved.

## Machine Learning Workflow

The general workflow followed in the practical assignments is:

1. Load the dataset.
2. Explore the data and identify potential issues.
3. Clean and preprocess the features.
4. Separate features from the target variable.
5. Split the data into training and testing sets.
6. Train a baseline model.
7. Evaluate the model using suitable metrics.
8. Compare alternative models or feature sets.
9. Analyze results and document conclusions.

Preprocessing steps that learn parameters from the data should be fitted on the training set only. Using pipelines helps prevent data leakage and makes experiments more reproducible.

## Key Learning Outcomes

By completing these assignments, the project demonstrates practical experience with:

- Exploratory data analysis and statistical summaries.
- Feature correlation and multicollinearity.
- Data preprocessing and feature transformations.
- Regression and classification.
- Text representation using TF-IDF.
- Naive Bayes, Decision Trees, and Random Forests.
- Model evaluation and error analysis.
- Hyperparameter tuning and feature importance.
- Reproducible experiments with Python and scikit-learn.

## Author

**Timur Abdikarimov**

Machine Learning coursework project.

GitHub: [Richeey01](https://github.com/Richeey01)

---

*This repository is intended for educational purposes. Results depend on the dataset, preprocessing choices, model configuration, and train/test split used in each notebook.*
