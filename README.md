# Project Title

## Introduction
This project includes a series of Python scripts for data preprocessing, cross-validation, model training, evaluation, and visualization, focusing on Elastic Net and Linear Regression models.

## Installation
### Prerequisites
- Python 3.x
- Libraries: numpy, pandas, matplotlib, scikit-learn

### Setup
Install the required libraries using:
```
pip install numpy pandas matplotlib scikit-learn
```

## File Descriptions
- **`data_preprocessing.py`:** Functions for data preprocessing, including standardization.
- **`cross_validation.py`:** Custom cross-validation functionality.
- **`elastic_net_model.py`:** Elastic Net regression model implementation.
- **`linear_regression_model.py`:** Linear Regression model implementation.
- **`plotting.py`:** Functions for plotting model results.
- **`consolidated.py`:** Integrates multiple functionalities for a unified workflow.
- **`main.py`:** Main runner script using command-line arguments for experiment execution.

## Usage
Run experiments using `main.py`. This script accepts command-line arguments to specify the data file and the desired operations.

### Example Commands
- **Run data preprocessing:**
```
python main.py gait.xlsx --run_preprocessing
```
```
Expected Result:
Running data preprocessing...
The shape of set of feature 1 is (84600, 126)
The shape of set of feature 2 is (84600, 175)
The shape of set of feature 3 is (84600, 105)
The shape of target y-value is (84600,)
Data Preprocessing completed.
```
```
Expected Running Time: 2 minutes
```
- **Run cross-validation:**
```
python main.py gait.xlsx --run_cross_validation
```
```
Expected Result:

```
```
Expected Running Time: 25 minutes
```
- **Run the Elastic Net model:**
```
python main.py gait.xlsx --run_elastic_net
```
```
Expected Result:

```
```
Expected Running Time: 25 minutes
```
- **Run the Linear Regression model:**
```
python main.py gait.xlsx --run_linear_regression
```
```
Expected Result:

```
```
Expected Running Time: 25 minutes
```
- **Generate plots:**
```
python main.py gait.xlsx --run_plot
```
```
Expected Result:

```
```
Expected Running Time: 25 minutes
```
- **Run all processes:**
```
python main.py gait.xlsx --run_all
```
```
Expected Result:

```
```
Expected Running Time: 25 minutes
```
