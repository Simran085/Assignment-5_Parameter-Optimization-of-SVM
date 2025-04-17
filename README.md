# Assignment-5_Parameter-Optimization-of-SVM

**## Wine Quality Classification Using SVM and Hyperparameter Tuning**
📌 **Objective**
This project aims to classify red wine quality using Support Vector Machines (SVM) and improve accuracy through hyperparameter tuning via RandomizedSearchCV.

📊 **Dataset**
**Source**: UCI Wine Quality Dataset (Red Wine)
**Features**: 11 physiochemical properties (e.g., acidity, sugar, pH).
**Target**: Wine quality (integer scores between 3 and 8).

⚙️ **Methodology**
**1. Data Loading & Preprocessing:**
   Loaded the dataset from UCI.
   Split features (X) and labels (y).
   Standardized the features using StandardScaler.

**2. Model Selection:**
   Used SVC (Support Vector Classifier) from sklearn.

**3. Hyperparameter Tuning:**
   Employed RandomizedSearchCV over 100 iterations per sample.
   Search space included:
     C: Range from 0.001 to 100 (logarithmic scale).
     kernel: ['linear', 'rbf', 'poly', 'sigmoid']
     gamma: ['scale', 'auto']
     degree: [2, 3, 4, 5] (relevant for polynomial kernel)

**4. Cross-Validation:**
  3-fold CV used to ensure robustness.
  Each experiment repeated across 10 different random seeds (random_state=0 to 9).

**5. Evaluation:**
   Recorded best accuracy and parameters for each split.
   Tracked convergence behavior of CV accuracy over 100 iterations.

📈 **Result Table**

![image](https://github.com/user-attachments/assets/8e98c05f-9bd9-4025-81c0-d8f2af38f603)


📉 **Convergence Graph**
The following graph shows the convergence behavior of the mean cross-validation accuracy during 100 random hyperparameter trials for the best-performing sample (S10):
   The graph illustrates the variation in mean CV scores over each iteration.
   Early iterations show fluctuations, but later iterations indicate more consistent high scores, suggesting convergence toward optimal parameter regions.

   ![image](https://github.com/user-attachments/assets/95c3c848-8ac1-47f2-b8e0-25fae499df40)


