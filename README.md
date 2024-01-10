# Advancing Gait Prediction: Feature Engineering in Linear and Elastic Net Approaches

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
Running cross validation...
The shape of set of feature 1 is (84600, 126)
The shape of set of feature 2 is (84600, 175)
The shape of set of feature 3 is (84600, 105)
The shape of target y-value is (84600,)
Data Preprocessing completed.

Running Elastic Net Model with Set of Feature 1
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 194.49264323287966
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 194.47519405163894
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 194.46202596727605
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 194.4345881939427
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 194.4345881939427

Running Elastic Net Model with Set of Feature 2
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 2.5345945002126777
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 2.4148703427986282
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 3.9819830180544145
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 3.8025567938678093
Best Parameters - alpha: 0.1, l1_ratio: 0.2, Best Mean Squared Error: 2.4148703427986282

Running Elastic Net Model with Set of Feature 3
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 245.4091206684643
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 245.38882770399795
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 245.37902493803813
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 245.3438605317951
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 245.3438605317951

Running Linear Regression Model with Set of Feature 1
fit_intercept=True, Mean Squared Error: 194.76433496363273
fit_intercept=False, Mean Squared Error: 342.5776674067766
Best fit_intercept: True, Best Mean Squared Error: 194.76433496363273

Running Linear Regression Model with Set of Feature 2
fit_intercept=True, Mean Squared Error: 4.408963673059245e-06
fit_intercept=False, Mean Squared Error: 147.60675169834946
Best fit_intercept: True, Best Mean Squared Error: 4.408963673059245e-06

Running Linear Regression Model with Set of Feature 3
fit_intercept=True, Mean Squared Error: 245.39110368183728
fit_intercept=False, Mean Squared Error: 554.2600949787671
Best fit_intercept: True, Best Mean Squared Error: 245.39110368183728
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
Running Elastic Net model...
The shape of set of feature 1 is (84600, 126)
The shape of set of feature 2 is (84600, 175)
The shape of set of feature 3 is (84600, 105)
The shape of target y-value is (84600,)
Data Preprocessing completed.

Running Elastic Net Model with Set of Feature 1
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 194.4926432328797
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 194.47519405163897
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 194.46202596727602
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 194.4345881939427
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 194.4345881939427

Running Elastic Net Model with Set of Feature 2
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 2.534594500212677
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 2.41487034279863
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 3.9819830180544096
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 3.8025567938678115
Best Parameters - alpha: 0.1, l1_ratio: 0.2, Best Mean Squared Error: 2.41487034279863

Running Elastic Net Model with Set of Feature 3
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 245.40912066846425
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 245.38882770399792
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 245.37902493803813
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 245.3438605317951
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 245.3438605317951

Running Linear Regression Model with Set of Feature 1
fit_intercept=True, Mean Squared Error: 194.9419217962485
fit_intercept=False, Mean Squared Error: 360.94692188717215
Best fit_intercept: True, Best Mean Squared Error: 194.9419217962485

Running Linear Regression Model with Set of Feature 2
fit_intercept=True, Mean Squared Error: 4.410769022092561e-06
fit_intercept=False, Mean Squared Error: 150.84811364522815
Best fit_intercept: True, Best Mean Squared Error: 4.410769022092561e-06

Running Linear Regression Model with Set of Feature 3
fit_intercept=True, Mean Squared Error: 245.73581860077735
fit_intercept=False, Mean Squared Error: 1580.558691740434
Best fit_intercept: True, Best Mean Squared Error: 245.73581860077735

The MSE of Elastic Net Model with Set of Feature 1: 215.6777147776531
The MSE of Elastic Net Model with Set of Feature 2: 2.4868041259874225
The MSE of Elastic Net Model with Set of Feature 3: 284.79446086692275

Elastic Net Model Completed
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
Running Linear Regression model...
The shape of set of feature 1 is (84600, 126)
The shape of set of feature 2 is (84600, 175)
The shape of set of feature 3 is (84600, 105)
The shape of target y-value is (84600,)
Data Preprocessing completed.

Running Elastic Net Model with Set of Feature 1
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 194.4926432328797
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 194.47519405163897
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 194.46202596727602
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 194.4345881939427
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 194.4345881939427

Running Elastic Net Model with Set of Feature 2
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 2.534594500212677
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 2.41487034279863
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 3.9819830180544096
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 3.8025567938678115
Best Parameters - alpha: 0.1, l1_ratio: 0.2, Best Mean Squared Error: 2.41487034279863

Running Elastic Net Model with Set of Feature 3
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 245.40912066846425
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 245.38882770399792
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 245.37902493803813
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 245.3438605317951
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 245.3438605317951

Running Linear Regression Model with Set of Feature 1
fit_intercept=True, Mean Squared Error: 194.9419217962485
fit_intercept=False, Mean Squared Error: 360.94692188717215
Best fit_intercept: True, Best Mean Squared Error: 194.9419217962485

Running Linear Regression Model with Set of Feature 2
fit_intercept=True, Mean Squared Error: 4.410769022092561e-06
fit_intercept=False, Mean Squared Error: 150.84811364522815
Best fit_intercept: True, Best Mean Squared Error: 4.410769022092561e-06

Running Linear Regression Model with Set of Feature 3
fit_intercept=True, Mean Squared Error: 245.73581860077735
fit_intercept=False, Mean Squared Error: 1580.558691740434
Best fit_intercept: True, Best Mean Squared Error: 245.73581860077735

The MSE of Linear Regression Model with Set of Feature 1: 215.62764988099207
The MSE of Linear Regression Model with Set of Feature 2: 3.1796820034441606e-06
The MSE of Linear Regression Model with Set of Feature 3: 284.9356776494888

Linear Regression Model Completed
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
Running All Codes...
The shape of set of feature 1 is (84600, 126)
The shape of set of feature 2 is (84600, 175)
The shape of set of feature 3 is (84600, 105)
The shape of target y-value is (84600,)
Data Preprocessing completed.

Cross Validation is Performing

Running Elastic Net Model with Set of Feature 1
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 194.4926432328797
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 194.47519405163897
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 194.46202596727602
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 194.4345881939427
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 194.4345881939427

Running Elastic Net Model with Set of Feature 2
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 2.534594500212677
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 2.41487034279863
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 3.9819830180544096
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 3.8025567938678115
Best Parameters - alpha: 0.1, l1_ratio: 0.2, Best Mean Squared Error: 2.41487034279863

Running Elastic Net Model with Set of Feature 3
alpha=0.1, l1_ratio=0.1, Mean Squared Error: 245.40912066846425
alpha=0.1, l1_ratio=0.2, Mean Squared Error: 245.38882770399792
alpha=0.2, l1_ratio=0.1, Mean Squared Error: 245.37902493803813
alpha=0.2, l1_ratio=0.2, Mean Squared Error: 245.3438605317951
Best Parameters - alpha: 0.2, l1_ratio: 0.2, Best Mean Squared Error: 245.3438605317951

Running Linear Regression Model with Set of Feature 1
fit_intercept=True, Mean Squared Error: 194.9419217962485
fit_intercept=False, Mean Squared Error: 360.94692188717215
Best fit_intercept: True, Best Mean Squared Error: 194.9419217962485

Running Linear Regression Model with Set of Feature 2
fit_intercept=True, Mean Squared Error: 4.410769022092561e-06
fit_intercept=False, Mean Squared Error: 150.84811364522815
Best fit_intercept: True, Best Mean Squared Error: 4.410769022092561e-06

Running Linear Regression Model with Set of Feature 3
fit_intercept=True, Mean Squared Error: 245.73581860077735
fit_intercept=False, Mean Squared Error: 1580.558691740434
Best fit_intercept: True, Best Mean Squared Error: 245.73581860077735

The MSE of Elastic Net Model with Set of Feature 1: 215.6777147776531
The MSE of Elastic Net Model with Set of Feature 2: 2.4868041259874225
The MSE of Elastic Net Model with Set of Feature 3: 284.79446086692275

Elastic Net Model Completed

The MSE of Linear Regression Model with Set of Feature 1: 215.62764988099207
The MSE of Linear Regression Model with Set of Feature 2: 3.1796820034441606e-06
The MSE of Linear Regression Model with Set of Feature 3: 284.9356776494888

Linear Regression Model Completed
```
```
Expected Running Time: 25 minutes
```
