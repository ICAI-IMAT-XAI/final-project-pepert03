# Explainable AI (XAI) - German Credit Risk Case Study

## Project Overview
This project explores the application of Explainable AI (XAI) techniques to a credit risk scoring model using the **German Credit dataset** trained on a "Black Box" model (Random Forest).

## Directory Structure
- **`notebooks/`**: Contains the Jupyter notebooks for the experiments.
- **`report/`**: Contains the final report (`final_report.pdf`) and the generated images.
- **`data/`**: Folders for raw and processed data.
- **`models/`**: Saved models and pipelines.

## Requirements
The project dependencies are listed in `requirements.txt`.
To install the standard dependencies:
```bash
pip install -r requirements.txt
```

**Important:** The `alepython` library requires a specific installation from its GitHub development branch:
```bash
pip install git+https://github.com/MaximeJumelle/ALEPython.git@dev#egg=alepython
```

## How to Run the Experiments
Please execute the notebooks in the following order to reproduce the results:

1.  **`notebooks/01_Preprocessing.ipynb`**
    -   Loads the raw data from the UCI repository.

2.  **`notebooks/02_Modeling.ipynb`**
    -   Builds the baseline Random Forest model.
    -   Evaluates performance (ROC-AUC, Confusion Matrix).
    -   Saves the trained model pipeline.

3.  **`notebooks/03_XAI.ipynb`**
    -   **Global Explanations:** Permutation Feature Importance (PFI), Partial Dependence Plots (PDP), ALE Plots, SHAP Beeswarm.
    -   **Local Explanations:** SHAP Waterfall and LIME for individual predictions.
    -   Generates explainability plots for the report.

4.  **`notebooks/04_Accionability.ipynb`**
    -   **Fairness Audit:** Analyzes bias in the model (specifically Age bias).
    -   **Model Improvement Experiment:** Removes biased features and simplifies the model (using only the Top 10 features) to improve both fairness and performance (Accuracy and ROC-AUC).

## Final Report
The detailed analysis and narrative of the findings can be found in:
`report/final_report.pdf`
