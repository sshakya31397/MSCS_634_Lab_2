# KNN vs RNN Classifier on Wine Dataset

## Purpose
The purpose of this lab is to compare the performance of two classification algorithms—K-Nearest Neighbors (KNN) and Radius Neighbors (RNN)—on the Wine Dataset from the `sklearn` library.
This experiment explores how different parameter values (K in KNN, radius in RNN) affect classification accuracy, 
helping to develop a deeper understanding of model tuning and decision boundaries.

## Key Insights

- **KNN Performance:** The KNN model showed stable and high accuracy for multiple values of K. The best performance was observed at K = *[insert best K]* with an accuracy of *[insert accuracy]*.
- **RNN Performance:** The RNN model's accuracy was highly sensitive to the radius value. Some radius values resulted in no neighbors for certain test points, reducing accuracy significantly. The best performance was at radius = *[insert best radius]*.
- **Comparison:** KNN was generally more robust and easier to tune. RNN can work well but requires careful selection of the radius to avoid prediction failures.

## Challenges and Decisions

- Choosing appropriate radius values for RNN was challenging; some values caused the model to fail due to no neighbors being found. To handle this, the `outlier_label=-1` parameter was used and a try/except block was added.
- Normalization wasn't applied in this lab, but it may improve RNN performance as it is sensitive to feature scale.
- Visualization helped identify trends and compare model behavior clearly.
