# Human Activity Recognition Using Smartphone Sensor Data

## Project Overview
This project develops and compares machine-learning models to recognize human activities using smartphone sensor data. It follows the Knowledge Discovery in Databases (KDD) process and evaluates performance on two datasets from the UCI Machine Learning Repository: UCI HAR and UCI HAPT.

The project also examines how class imbalance affects recognition performance, particularly for rare postural transitions.

## Objectives
- Analyze the UCI HAR and UCI HAPT datasets.
- Perform data-quality checks and prepare features and activity labels for modelling.
- Compare Logistic Regression, k-Nearest Neighbors (k-NN), Decision Tree, and Random Forest.
- Select the best model using validation macro F1-score.
- Evaluate the selected model using accuracy, precision, recall, macro F1-score, and confusion matrices.
- Analyze class-level errors and feature importance.

## Datasets

1. **UCI HAR:** [Human Activity Recognition Using Smartphones](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones)
   - Training samples: 7,352
   - Test samples: 2,947
   - Features: 561
   - Classes: 6

2. **UCI HAPT:** [Smartphone-Based Recognition of Human Activities and Postural Transitions](https://archive.ics.uci.edu/dataset/341/smartphone+based+recognition+of+human+activities+and+postural+transitions)
   - Training samples: 7,767
   - Test samples: 3,162
   - Features: 561
   - Classes: 12

## Methodology
The project follows these KDD stages:
1. Data selection
2. Data understanding
3. Data preprocessing and transformation
4. Data mining and model development
5. Model evaluation and selection
6. Knowledge presentation

Data-quality checks were performed for missing feature values and duplicate training feature rows. The official train/test partitions were preserved, a stratified validation split was created from the training data, and scaling was applied where required.

## Machine-Learning Models
- **Logistic Regression:** Baseline classification model.
- **k-Nearest Neighbors (k-NN):** Distance-based classification model.
- **Decision Tree:** Tree-based classification model.
- **Random Forest:** Ensemble classification model selected for final testing based on validation macro F1-score.

## Results

Random Forest achieved the highest validation macro F1-score among the four tested models on both datasets.

| Dataset | Test Accuracy | Test Macro F1-Score |
|---|---:|---:|
| UCI HAR | 92.84% | 92.66% |
| UCI HAPT | 91.14% | 82.25% |

The results show that basic activities are recognized comparatively well. The lower macro F1-score on HAPT highlights the difficulty of classifying rare postural transitions. Confusion matrices and feature-importance plots were also used to interpret model performance.

## Technologies Used
- Python
- Jupyter Notebook / Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib


## Future Scope
- Improve recognition of rare postural-transition classes.
- Evaluate additional machine-learning and deep-learning models.
- Test generalization using independent datasets and subject-wise validation.
- Explore explainability techniques and raw-sensor deep-learning approaches.

## Author
**Ravi Kumar Kushwaha**  
B.Tech Computer Science and Engineering  
Symbiosis Institute of Technology, Nagpur  
Batch: 2023–2027 | Semester 7 | Section B
