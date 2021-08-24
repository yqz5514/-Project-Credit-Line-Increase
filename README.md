# Credit Line Increase Model Card

### Basic Information

* **Person or organization developing model**: Zaurez Hamid, Senay Kefela, Suyash Shrivastava, Yaxin(Janet) Zhuang
* **Model date**: August, 2021
* **Model version**: 1.0
* **License**: Apache-2.0 License
* **Model implementation code**:

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

### Model Card Project Deliverable (40 pts.):
In your new Github repository, use GitHub Markdown to transform your README.md file into a
model card. (Each group only needs one repository.) Ensure your model card follows these
bullet points:
● Basic information (6 pts.):
○ Group member names and emails (you may use first names and anonymous
emails, for example: Patrick, patrick@acme.com)
○ Date
○ Model version
○ License (please use an MIT or Apache 2.0 License)
○ Model implementation code (link to Jupyter notebook)
○ Intended Use:
■ Intended uses
■ Intended users
■ Out-of-scope uses
● Training data (8 pts.):
○ Source of training data
○ How training data was divided into training and validation data
○ Number of rows in training and validation data
○ Data dictionary; for each column in the training dataset include:
■ Name
■ Modeling role
■ Measurement level
■ Description
● Test data (5 pts.):
○ Source of test data
○ Number of rows in test data
○ State any differences in columns between training and test data
● Model details (8 pts.):
○ Columns used as inputs in the final model
○ Column(s) used as target(s) in the final model
○ Type of model
○ Software used to implement the model
○ Version of the modeling software
○ Hyperparameters or other settings of your model
● Quantitative analysis (7 pts.):
○ Metrics used to evaluate your final model
○ State the final values of the metrics for all data: training, validation, and test data
○ Provide any plots related to your data or final model -- be sure to label the plots!
● Ethical considerations (6 pts.):
○ Describe potential negative impacts of using your model:
■ Math or software problems
■ Real-world risks: who, what, when or how
○ Describe potential uncertainties relating to the impacts of using your model:
■ Math or software problems
■ Real-world risks: who, what, when or how?
○ Describe any unexpected or results
