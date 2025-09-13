# Basketball-Strike-Zone

⚾ Predicting Basketball Strike Zones with Machine Learning
📌 Project Overview

This project uses machine learning classification to predict whether a pitch is a ball or a strike based on its location over home plate. The model simulates an umpire’s decision-making process by analyzing historical pitch data.

The project demonstrates skills in data preprocessing, visualization, supervised learning, and model evaluation using Python and scikit-learn.

🛠️ Key Concepts & Skills

Data Exploration & Visualization: Analyze pitch coordinates (plate_x, plate_z) and their relation to strike/ball calls.

Data Preprocessing: Clean data, handle missing values, and convert categorical descriptions into numerical labels.

Model Building: Train a Support Vector Machine (SVM) classifier to separate strikes from balls.

Decision Boundary Visualization: Visualize the strike zone using Matplotlib/Seaborn.

Model Evaluation: Measure accuracy and tune hyperparameters (C, gamma).

📂 Dataset

The dataset includes information about pitch locations and umpire decisions. Example columns:

plate_x → Horizontal position of the pitch

plate_z → Vertical position of the pitch

description → Pitch result (S = Strike, B = Ball)

🧮 Data Structures Used

pandas DataFrame → For data loading and preprocessing

NumPy arrays → For feature/label extraction

scikit-learn objects → SVM classifier, train/test splits, accuracy metrics

📊 Workflow

Load Data
Import pitch data (CSV) using pandas.

Preprocess Data

Drop missing values

Encode categorical labels (S → 1, B → 0)

Split Data

Training set (80%)

Test set (20%)

Train Model

Use sklearn.svm.SVC with RBF kernel

Tune hyperparameters (C, gamma)

Evaluate Model

Check accuracy on test set

Compare predictions vs. actual calls

Visualize Strike Zone

Scatterplot of pitch locations

Overlay decision boundary from the trained SVM

📈 Time Complexity

Training (SVM, RBF Kernel):
~ 
𝑂
(
𝑛
2
⋅
𝑑
)
O(n
2
⋅d) to 
𝑂
(
𝑛
3
)
O(n
3
), where 
𝑛
n = number of pitches, 
𝑑
d = features (2).

Prediction:
~ 
𝑂
(
𝑛
⋅
𝑑
)
O(n⋅d) per pitch.