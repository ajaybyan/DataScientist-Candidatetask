# DataScientist-Candidatetask

python version = 3.9.15

Packages installed with conda installation.

## Files  
- 1.Data_understanding : jupyter notebook for performing data understanding task.  
- 2.Modeling: jupyter notebook to perform the modeling task
- requirements.txt : list of packages


### Part 1: Baseline model and analysis
- Data Investigation: A quick data investigation was performed to check the data types, missing values and investigate distribution of each features to understand their possible impact in the modeling.
- Possible irrelevant features were dtermined during feature exploration.
- Some input feature and target relation was analyzed to get an understanding of the possible feature importance in the modeling.
  #### Data Preprocessing performed
  - Dropped features with constant value.
  - Dropped co-rrelated features (features representing same information)
  - Dropped records with missing values
  - Rare label encoding for the target features 'TILI' and 'ALV-KOODI'

  ### Modeling
  Modeling performed with multi-layer perceptron nerural network with tensoflow-keras
  - The choice of neural network with keras was made for a simple reason that it could handle multi-ouptut modeling.
  - For the model tuning, trial and error method was used to tune the 'learning rate' and 'epochs' parameters.
    - Best learnin rate = 0.001 and best epochs = 200
    ##### Modling results on the test data:
    - TILI - Loss: 1.4177
    - TILI - Accuracy: 0.5987
    - ALV-KOODI - Loss: 0.0679
    - ALV-KOODI - Accuracy: 0.978



 ### Part 2: Questions
1. Assuming the task completion time would be longer, let's say two months. What additional steps would you take?
- Given a longer time, I would spend more time on data exploration and feature engineering. Try different feature transformation methods specially on the very largely skewed features. Also, spend extra time on trying multiple models for the modeling and fine tuning the model and possibly ensemble modeling too. 
2. If you had access to a domain expert (e.g. customer, accountant), what questions would you ask them?
- Firstly, I would ask for the reasons for the missing data if there are many of them. Ask the reason why some features were highly skewed, specially the target features to understand the practical context and treat them accordingly. Also, I would try to know from their experience if they see any regural pattern that we could consider in the modeling.

3. How would you add the domain expert knowledge to the solution?
- Having the domain expert knowledge is very useful in the data preparation phase, where we can create new features through feature engineering based on our domain knowledge. In this particular exercise the high skewness in the target feature was very surprising and with the domain expert we would have better knowledge on hadling the feature. With the domain knowledge when we have more experience on what is the desire outcome, it can be helpful in how we formulate our modeling approach. We could formulate our modeling approach in multiple steps if that helps in solving our problem rather than just relying on a single model.
