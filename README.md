# Applied Machine Learning

A hands-on **Applied Machine Learning** project covering classification, regression, and clustering on real-world scientific datasets.

The project focuses on the practical challenges of building and optimising machine learning models: selecting relevant variables, comparing different model families, evaluating performance, and developing complete solutions under constraints where performance on the final test data is unknown.

This project was developed as part of an Applied Machine Learning course at the **Niels Bohr Institute (NBI), University of Copenhagen**.

## Project Overview

The assignment was designed to reproduce a realistic machine learning scenario in which models must be optimised without directly observing their performance on the data used for final evaluation.

The project covers three different machine learning tasks:

- **Classification** — predicting discrete target classes from particle-physics data.
- **Regression** — predicting continuous quantities from particle-physics data.
- **Clustering** — identifying structure and groups in astronomical data.

A major component of the project was **feature selection**. Although the datasets contained a large number of available input variables, the objective was not to use all of them. Instead, relevant variables had to be identified separately for each task.

## Project Objectives

The project was designed around several practical machine learning challenges:

1. **Model optimisation** without access to final test-set performance.
2. **Independent implementation** of machine learning algorithms.
3. Comparison between **tree-based and neural-network-based models**.
4. **Feature selection** and investigation of which variables are relevant for each task.
5. Consideration of both **model performance and computational size**.
6. Building complete, working ML solutions rather than focusing solely on theoretical models.

The course description specifically emphasised trying both tree-based and neural-network approaches and thinking critically about the models and variables used.

## Datasets

The project uses scientific datasets originating from two domains.

### Classification & Regression

The classification and regression datasets come from **particle physics**.

The available data consists of:

| Dataset | Number of observations |
|---|---:|
| Training set | 180,000 |
| Classification test set | 60,000 |
| Regression test set | 40,000 |

### Clustering

The clustering dataset comes from **astronomy**.

| Dataset | Number of observations |
|---|---:|
| Clustering training/testing data | 8,000 |

The assignment provides a large number of potential input variables, but explicitly requires students to identify a smaller relevant subset for each problem. The target numbers were **25 variables for classification, 12 for regression, and 7 for clustering**.

## Machine Learning Tasks

### 1. Classification

The classification task is formulated as a supervised learning problem using particle-physics data.

The goal is to develop a model capable of assigning observations to the appropriate class while achieving strong performance on unseen data.

The classification workflow includes:

```text
Particle Physics Data
        ↓
Exploratory Analysis
        ↓
Feature Selection
        ↓
Preprocessing
        ↓
Model Development
        ↓
Hyperparameter / Model Optimisation
        ↓
Classification
        ↓
Performance Evaluation
```

Different modelling approaches are investigated, with particular emphasis on comparing tree-based and neural-network-based algorithms.

The final performance is evaluated using **cross-entropy**, which was also used in the course's project scoring scheme.

### 2. Regression

The regression task uses particle-physics data to predict a continuous target.

The modelling process follows a similar structure:

```text
Particle Physics Data
        ↓
Exploratory Analysis
        ↓
Feature Selection
        ↓
Preprocessing
        ↓
Regression Models
        ↓
Model Optimisation
        ↓
Predictions
        ↓
Error Analysis
```

Model performance is evaluated on unseen data, with the project assessment based on the relative prediction error through the **Mean Absolute Deviation (MAD)** formulation specified in the assignment.

### 3. Clustering

The clustering task uses an **astronomical dataset** and addresses an unsupervised learning problem.

Unlike classification and regression, clustering does not rely on a predefined target during model training. Instead, the objective is to identify meaningful groups within the observations.

The workflow is:

```text
Astronomical Data
        ↓
Exploratory Analysis
        ↓
Feature Selection
        ↓
Preprocessing
        ↓
Clustering
        ↓
Cluster Analysis
        ↓
Evaluation
```

The project specifically limits the selected feature set for clustering to the most relevant variables rather than using every available input.

## Feature Selection

Feature selection is an important part of the project.

Rather than treating every available variable as equally useful, the analysis investigates which features provide meaningful information for each machine learning task.

The project therefore uses different feature subsets for:

```text
Classification → 25 variables
Regression     → 12 variables
Clustering     → 7 variables
```

This reflects an important practical ML principle: **more features do not necessarily mean a better model**.

Reducing the feature space can improve model efficiency, reduce unnecessary complexity, and potentially improve generalisation.

## Model Comparison

An important requirement of the project was to gain practical experience with different model families.

In particular, the project compares:

- **Tree-based machine learning algorithms**
- **Neural-network-based algorithms**

The objective was not simply to identify the theoretically most sophisticated algorithm, but to understand the practical differences between approaches and optimise models for the given tasks.

## Evaluation

The project evaluates each task using the performance measures specified for the assignment.

For classification, the scoring system is based on **cross-entropy**.

For regression, performance is based on the **Mean Absolute Deviation (MAD)** of the relative prediction error.

For clustering, the scoring system uses **accuracy** relative to the clustering results.

The assignment also considers the quality of the selected variables and the range of algorithms used, rather than evaluating performance alone.

## Repository Structure

```text
applied-machine-learning/
│
├── Classification.ipynb
│   └── Classification analysis and model development
│
├── Regression.ipynb
│   └── Regression analysis and model development
│
├── Clustering_Applied_ML.ipynb
│   └── Clustering analysis on astronomical data
│
└── README.md
```

The repository contains the three main notebooks corresponding to the three project tasks.

## Technologies

The project is implemented in **Python** using Jupyter Notebooks.

Key technologies and concepts include:

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Scikit-learn
- Machine Learning
- Classification
- Regression
- Clustering
- Feature Selection
- Model Optimisation
- Tree-based Models
- Neural Networks
- Data Visualisation

## Getting Started

Clone the repository:

```bash
git clone https://github.com/mohmmadhadi/applied-machine-learning.git
cd applied-machine-learning
```

Install the main dependencies:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

Launch Jupyter:

```bash
jupyter notebook
```

Then open the notebook corresponding to the task you want to explore:

```text
Classification.ipynb
Regression.ipynb
Clustering_Applied_ML.ipynb
```

Run the notebooks sequentially to reproduce the analysis.

## Results

The project evaluates models based on both predictive performance and modelling decisions.

The assessment framework considers:

- Classification performance
- Regression performance
- Clustering performance
- Feature selection
- Number and choice of algorithms
- Completeness of the submitted solution
- Penalties for issues in the final solution

The original project brief explicitly states that the emphasis is on delivering **good working solutions rather than perfection**.

## Key Takeaways

This project demonstrates several important aspects of applied machine learning:

- Model optimisation is often performed without knowing final test performance.
- Feature selection is an important part of model development.
- Different ML algorithms can behave very differently on the same task.
- Tree-based models and neural networks offer different strengths and trade-offs.
- Classification, regression, and clustering require different modelling strategies.
- Practical ML involves not only model selection, but also preprocessing, feature engineering, optimisation, evaluation, and careful consideration of computational complexity.

## Course Context

The project was part of an Applied ML initial project whose goal was to ensure that students independently implemented and applied machine learning algorithms rather than simply relying on pre-built solutions.

The course project required complete solutions for classification, regression, and clustering and encouraged experimentation with different algorithms and model configurations.

## Author

**Mohammadhadi Shahhosseini**

MSc Data Science for Economics  
University of Milan

GitHub: [@mohmmadhadi](https://github.com/mohmmadhadi)

## License

This repository is intended for educational and portfolio purposes.
