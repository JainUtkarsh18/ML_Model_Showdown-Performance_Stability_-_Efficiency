# ML_Model_Showdown-Performance_Stability_Efficiency

A reusable machine learning benchmarking project for evaluating multiple classification algorithms across diverse datasets based on predictive performance, cross-validation stability, cross-dataset consistency, computational efficiency, and dataset characteristics.

The project demonstrates a systematic approach to machine learning model evaluation using standardized preprocessing, cross-validation, performance analysis, efficiency analysis, explainability, and dataset-level investigation.

---

## Kaggle Notebook

The original notebook 'ML Model Showdown: Performance & Stability' is available on [Kaggle](https://www.kaggle.com/code/utkarshjain76/ml-model-showdown-performance-stability).

The notebook is designed as an exploratory machine learning benchmarking study that evaluates multiple models across different classification datasets.

---

## Project Overview

This project investigates how different machine learning algorithms behave when evaluated across diverse datasets.

Instead of evaluating a model on a single dataset, the benchmark compares multiple algorithms across several datasets and studies:

* Predictive performance
* Cross-validation stability
* Cross-dataset consistency
* Training efficiency
* Prediction efficiency
* Dataset characteristics
* Feature-level importance

The primary research question is:

> **How does dataset structure influence the performance, consistency, and computational behaviour of different machine learning algorithms?**

The project treats model benchmarking as more than simply identifying the highest-performing model on a single dataset.

---

## Features

* Multi-dataset machine learning benchmarking
* Multiple classification algorithms
* OpenML dataset integration
* Automated dataset profiling
* Leakage-safe preprocessing
* Stratified cross-validation
* Performance evaluation
* Cross-dataset consistency analysis
* Training and prediction time analysis
* Dataset characteristic analysis
* Feature importance analysis
* Automated benchmark result exports
* Reproducible experimental workflow

---

## Benchmark Workflow

```text
OpenML Datasets
        │
        ▼
Dataset Selection
        │
        ▼
Dataset Profiling
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Leakage-Safe Preprocessing
        │
        ▼
Multi-Model Benchmark
        │
        ▼
Cross-Validation
        │
        ▼
Performance Analysis
        │
        ▼
Consistency Analysis
        │
        ▼
Efficiency Analysis
        │
        ▼
Explainability
        │
        ▼
Research Findings
```

This workflow follows the experimental structure implemented in the notebook.

---

## Datasets

The benchmark uses classification datasets retrieved from OpenML.

The evaluated datasets include:

* Adult Income
* Credit-G
* Spambase
* Diabetes
* Bank Marketing

The datasets contain different combinations of numerical and categorical features, dataset sizes, class distributions, missing values, duplicate observations, and other structural characteristics.

---

## Machine Learning Models

The benchmark evaluates the following model families:

* Dummy Classifier
* Logistic Regression
* K-Nearest Neighbours (KNN)
* Decision Tree
* Random Forest
* HistGradientBoosting
* Multi-Layer Perceptron (MLP)
* XGBoost
* LightGBM

The notebook evaluates **9 model families** across the benchmark datasets.

---

## Evaluation Metrics

The models are evaluated using multiple dimensions rather than relying on a single performance metric.

### Performance

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC

### Stability

* Cross-validation F1-score
* Cross-validation variability

### Efficiency

* Training time
* Prediction time

### Consistency

* Mean F1 across datasets
* Dataset ranking
* Ranking variability
* Number of datasets successfully evaluated

This allows predictive performance, stability, consistency, and computational efficiency to be examined separately.

---

## Benchmark Analysis

The project performs several levels of analysis.

### Model Performance

Compares predictive performance across datasets using standard classification metrics.

### Cross-Dataset Consistency

Measures whether models remain competitive when evaluated on different datasets.

The analysis considers mean F1, F1 variability, average dataset rank, ranking variability, and training time.

### Performance vs Efficiency

The project compares predictive performance against computational cost to investigate performance-efficiency trade-offs.

```text
Predictive Performance
          ↕
    Computational Cost
```

Training and prediction times are measured for each model to provide a more practical comparison.

### Dataset Characteristics

The benchmark investigates relationships between model performance and characteristics such as:

* Number of samples
* Number of features
* Numerical features
* Categorical features
* Number of classes
* Missing values
* Duplicate observations
* Class imbalance
* High-cardinality features

These relationships are treated as exploratory rather than causal.

---

## Output

The notebook generates benchmark results that can be exported as CSV files:

```text
dataset_profiles.csv
model_benchmark_results.csv
best_model_per_dataset.csv
cross_dataset_model_consistency.csv
model_efficiency_summary.csv
dataset_characteristics_vs_performance.csv
benchmark_failures.csv
```

The `benchmark_failures.csv` file is generated when benchmark failures are present.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* LightGBM
* Matplotlib
* OpenML
* Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone https://github.com/<your_username>/ml-model-showdown.git
```

Navigate to the project:

```bash
cd ml-model-showdown
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Launch the notebook:

```bash
jupyter notebook
```

Then open:

```text
ML_Model_Showdown_Performance,_Stability_&_Efficiency.ipynb
```

Since the notebook retrieves datasets programmatically from OpenML, Internet access is required during dataset retrieval.

---

## Project Structure

```text
ML-Model-Showdown/
│
├── ML_Model_⚔️_Showdown_Performance,_Stability_&_Efficiency.ipynb
│
├── dataset_profiles.csv
├── model_benchmark_results.csv
├── best_model_per_dataset.csv
├── cross_dataset_model_consistency.csv
├── model_efficiency_summary.csv
├── dataset_characteristics_vs_performance.csv
├── benchmark_failures.csv
│
├── requirements.txt
└── README.md
```

---

## Key Insight

The benchmark is designed around the idea that:

```text
Performance ≠ Consistency ≠ Efficiency
```

A model can perform strongly while being computationally expensive, while another model may achieve competitive performance with substantially lower computational cost.

The experiment therefore focuses on understanding **model behaviour across different data environments**, rather than treating a single benchmark score as a universal measure of model quality.

---

## Limitations

This project is intended as an **exploratory benchmark**, rather than a definitive ranking of machine learning algorithms.

Current limitations include:

* Limited selection of OpenML datasets
* Mostly default or lightly specified hyperparameters
* Exploratory rather than causal dataset-performance analysis
* Training times dependent on the execution environment
* Dependence on OpenML availability and Internet access
* No direct evaluation of fairness, calibration, robustness, or domain suitability

---

## Future Improvements

* Expand the benchmark to more OpenML datasets
* Add systematic hyperparameter optimization
* Include additional machine learning algorithms
* Add statistical significance testing
* Add model calibration analysis
* Add robustness and distribution-shift testing
* Add fairness evaluation
* Improve automated dataset meta-feature analysis
* Build an interactive benchmarking dashboard
* Add automated testing and CI/CD

---

## References

* OpenML — Dataset collections, metadata, and benchmark infrastructure
* Scikit-learn — Cross-validation and model evaluation
* Scikit-learn — Permutation Feature Importance
* Breiman, L. (2001). *Random Forests*. Machine Learning, 45, 5–32.

The notebook contains the detailed references and benchmarking methodology.

---

## License

This project is licensed under the MIT License.

---

I am open to collaborations, suggestions, and recommendations for extending this benchmarking project.
