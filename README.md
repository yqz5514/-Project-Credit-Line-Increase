# Credit Line Increase Model Card

### Basic Information

* **Person or organization developing model**: Zaurez Hamid (zaurez@gwu.edu), Senay Kefela (senayk@gwu.edu), Suyash Shrivastava (suyash65@gwu.edu), Yaxin(Janet) Zhuang (yxzhuang27@gwu.edu)
* **Model date**: August, 2021
* **Model version**: 1.0
* **License**: Apache-2.0 License
* **Model implementation code**: [Group13_DNSC_6301_Project.ipynb](Group13_DNSC_6301_Project.ipynb)
### Intended Use
* **Primary intended uses**: This model is an *example* probability of default classifier, with an *example* use case for determining eligibility for a credit line increase.
* **Primary intended users**: Students in GWU DNSC 6301 bootcamp.
* **Out-of-scope use cases**: Any use beyond an educational example is out-of-scope.

### Training Data

* Data dictionary: 

| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
|**ID**| ID | int | unique row indentifier |
| **LIMIT_BAL** | input | float | amount of previously awarded credit |
| **SEX** | demographic information | int | 1 = male; 2 = female
| **RACE** | demographic information | int | 1 = hispanic; 2 = black; 3 = white; 4 = asian |
| **EDUCATION** | demographic information | int | 1 = graduate school; 2 = university; 3 = high school; 4 = others |
| **MARRIAGE** | demographic information | int | 1 = married; 2 = single; 3 = others |
| **AGE** | demographic information | int | age in years |
| **PAY_0, PAY_2 - PAY_6** | inputs | int | history of past payment; PAY_0 = the repayment status in September, 2005; PAY_2 = the repayment status in August, 2005; ...; PAY_6 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; ...; 8 = payment delay for eight months; 9 = payment delay for nine months and above |
| **BILL_AMT1 - BILL_AMT6** | inputs | float | amount of bill statement; BILL_AMNT1 = amount of bill statement in September, 2005; BILL_AMT2 = amount of bill statement in August, 2005; ...; BILL_AMT6 = amount of bill statement in April, 2005 |
| **PAY_AMT1 - PAY_AMT6** | inputs | float | amount of previous payment; PAY_AMT1 = amount paid in September, 2005; PAY_AMT2 = amount paid in August, 2005; ...; PAY_AMT6 = amount paid in April, 2005 |
| **DELINQ_NEXT**| target | int | whether a customer's next payment is delinquent (late), 1 = late; 0 = on-time |

* **Source of training data**: GWU Blackboard, email `jphall@gwu.edu` for more information
* **How training data was divided into training and validation data**: 50% training, 25% validation, 25% test
* **Number of rows in training and validation data**:
  * Training rows: 15,000
  * Validation rows: 7,500

### Test Data
* **Source of test data**: GWU Blackboard, email `jphall@gwu.edu` for more information
* **Number of rows in test data**: 7,500
* **State any differences in columns between training and test data**: None

### Model details:
* **Columns used as inputs in the final model**: 
  * Limit_BAL
  * PAY_0, PAY_2, PAY_3, PAY_4, PAY_5, PAY_6
  * BILL_AMT1, BILL_AMT2, BILL_AMT3, BILL_AMT4, BILL_AMT5, BILL_AMT6
  * PAY_AMT1, PAY_AMT2, PAY_AMT3, PAY_AMT4, PAY_AMT5, PAY_AMT6
* **Columns used as targets in the final model**: DELINQ_NEXT
* **Type of Model**: Supervised Learning - Decision Tree Model
* **Software used to train the Model**: Python via Google Colab
* **Version of the Software used to train the Model**: Python 3.6.9
* **Hyperparameters or other settings of the model**: ***TO FILL OUT***
### Quantitative analysis:
* **Metrics used to evaluate the model and final figures**:
  * **Training AUC**: 0.78
  * **Validation AUC**: 0.75
  * **Test AUC**: 0.74
  * **Asian-to-White AIR**: 1.02
  * **Black-to-White AIR**: 0.81
  * **Female-to-Male AIR**: 1.04
  * **Hispanic-to-White AIR**: 0.83
* **Iteration Plot of the final model (inclusive of Training AUC, Validation AUC and Hispanic-to-White AIR**: ![download](https://github.com/yqz5514/DNSC6301-Group-Project-by-Group-13/blob/main/iterationplot.JPG)
### Ethical considerations:
* **Describe potential negative impacts of using your model:** 
  * Math or software problems:
  * Real-world risks:
* **Describe potential uncertainties relating to the impacts of using your model:**
  * Math or software problems
  * Real-world risks:
* **Describe any unexpected or results**
