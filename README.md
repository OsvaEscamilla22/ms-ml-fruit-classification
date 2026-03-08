# MS ML Fruit Classification

## Objective
This project was developed as part of my Master's in Data Science coursework in the Artificial Intelligence for Data Science subject. The objective was to build and evaluate a supervised machine learning model capable of classifying different fruit types from physical, sensory, and economic attributes. From a portfolio perspective, this project also reflects how I connect Data Science with a Food Science mindset by translating product-related variables into a structured classification problem.

## Dataset
The dataset is an academic structured dataset containing 10,000 fruit observations. Each record represents one fruit instance and includes both numerical and categorical variables commonly associated with food raw-material characterization.

**Target variable**
- `fruit_name`

**Predictor variables**
- `size (cm)`
- `weight (g)`
- `avg_price (₹)`
- `shape`
- `color`
- `taste`

The notebook includes initial data inspection, duplicate removal, descriptive statistics, and an exploratory discussion about outlier treatment. A key analytical finding was that global IQR-based outlier removal can distort class representation by eliminating valid observations from naturally larger fruits such as pineapple, papaya, coconut, and watermelon.

## Methodology
The project followed a standard machine learning workflow:

1. **Data loading and inspection** to validate schema and review the initial structure.
2. **Data cleaning** focused on duplicate removal and exploratory outlier analysis.
3. **Exploratory data analysis** for numerical and categorical variables using descriptive summaries and visualizations.
4. **Preprocessing pipeline** combining:
   - `StandardScaler` for numerical features
   - `OrdinalEncoder` for categorical features
5. **Train-test split** to separate training and evaluation data.
6. **Model training** using a `RandomForestClassifier`.
7. **Model evaluation** through accuracy, confusion matrix, and classification report.
8. **Prediction examples** to simulate simple decision-support and recommendation use cases.

Additionally, the notebook documents an experimental reflection on three possible data-treatment strategies:
- Baseline with duplicate removal only
- Global IQR outlier removal
- Class-conditional IQR outlier removal

This strengthens the project because it shows not only model execution, but also critical thinking about data quality and representativeness.

## Tools
- Python
- pandas
- NumPy
- matplotlib
- seaborn
- scikit-learn
- Jupyter / Google Colab

## Key Insights
The model achieved perfect performance on the evaluated holdout split, with 1.00 accuracy and 1.00 macro F1 across the reported classes. While this is a strong academic result, it should be interpreted carefully in portfolio terms because it suggests the dataset is highly separable and may be synthetic or simplified for instructional purposes.

A more interesting insight comes from the data preparation stage: applying global IQR filtering across numerical variables can remove entire fruit classes that legitimately differ in scale, which creates bias and reduces representativeness. This makes the project valuable not only as a classification exercise, but also as an example of why preprocessing decisions must be aligned with domain knowledge.

## Results
- **Model:** Random Forest Classifier
- **Reported accuracy:** 1.00
- **Reported macro F1-score:** 1.00
- **Classes evaluated:** 16 fruit categories
- **Additional outputs:** confusion matrix, classification report, feature importance visualization, single-sample prediction, and preference-based recommendation example

From a business or applied perspective, this type of workflow can be connected to raw-material screening, ingredient characterization, and decision-support systems where categorical product identification is required from measurable attributes.

## Repository Structure
```text
ms-ml-fruit-classification/
├── README.md
├── data/
├── notebooks/
│   └── fruit_classification_and_characterization_ml.ipynb
├── src/
├── outputs/
├── images/
├── requirements.txt
└── .gitignore
```

- `data/`: raw or processed datasets used in the project
- `notebooks/`: exploratory and modeling notebooks
- `src/`: reusable scripts for preprocessing, training, or inference
- `outputs/`: exported metrics, tables, and model artifacts
- `images/`: charts or screenshots used in the README

## Notes for Portfolio Positioning
This repository is presented as an **academic machine learning project** completed during my Master's in Data Science. Its value in my portfolio lies in showing:
- my end-to-end ML workflow
- my ability to connect data preprocessing with domain interpretation
- my hybrid profile as a Data Scientist with a Food Science background

## References
- https://www.kaggle.com/datasets/pranavkapratwar/fruit-classification

## Author
**Osvaldo Gil Escamilla**  
Data Scientist with a Food Science background  
Personal brand: **Data Food Solutions**
