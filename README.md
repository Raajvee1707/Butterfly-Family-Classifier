# 🦋 Butterfly Family Classification Using Machine Learning

## Project Overview

This project uses machine learning to classify butterflies into six families based on recorded biological traits from the **LepTraits dataset**. Two classification algorithms, Decision Tree and K-Nearest Neighbors (KNN), are implemented and compared. Hyperparameter tuning is performed to explore whether adjusting model settings improves classification performance.

## Objective

- Prepare and analyze a real-world biological dataset.
- Predict butterfly family using selected biological features.
- Implement and compare Decision Tree and KNN classifiers.
- Apply hyperparameter tuning using five-fold cross-validation.
- Evaluate model performance using accuracy and confusion matrices.

## Dataset

The project uses the [LepTraits dataset](https://github.com/RiesLabGU/LepTraits), specifically the `consensus.csv` file.

The dataset contains **12,448 records and 43 columns**, including butterfly taxonomy, wingspan measurements, flight periods, and host-plant associations.

### Features Used

- `WS_U` — upper wingspan measurement
- `NumberOfHostplantFamilies` — number of associated host-plant families
- `PrimaryHostplantFamily` — recorded primary host-plant family
- `SecondaryHostplantFamily` — recorded secondary host-plant family

**Target variable:** `Family`

The model predicts one of six butterfly families: Hesperiidae, Lycaenidae, Nymphalidae, Papilionidae, Pieridae, or Riodinidae.

## Methodology

1. **Data loading and exploration:** Load the CSV dataset using Pandas and inspect its structure and missing values.
2. **Feature selection:** Select biological traits as input features and `Family` as the target.
3. **Data preparation:** Impute missing values, encode categorical variables using one-hot encoding, and standardize numerical features.
4. **Train-test split:** Divide the data into training and testing sets using an 80:20 split, with stratification by family.
5. **Model building:** Train Decision Tree and KNN classifiers.
6. **Hyperparameter tuning:** Use `GridSearchCV` with five-fold cross-validation to explore model configurations.
7. **Evaluation:** Compare test accuracy and examine confusion matrices and classification reports.

## Models and Results

| Model | Test Accuracy |
|---|---:|
| Decision Tree (tuned) | 39.72% |
| K-Nearest Neighbors (tuned) | 44.06% |

KNN achieved the higher test accuracy in this experiment, outperforming the tuned Decision Tree by 4.34 percentage points.

The classification reports also revealed differences in performance across butterfly families. This demonstrates why accuracy should be considered alongside precision, recall, F1-score, and confusion matrices.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Google Colab
- GitHub

## How to Run

1. Download or clone this repository.
2. Open the `.ipynb` notebook in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.
3. Run the notebook cells in order.
4. Ensure an internet connection is available to load the dataset from GitHub.

The notebook downloads the dataset directly from the original repository, so a separate local CSV file is not required.

## Conclusion

This project demonstrates a complete introductory machine learning workflow, from data preparation and feature selection to model training, hyperparameter tuning, and evaluation. KNN performed better than the Decision Tree on the held-out test set, although both models showed limitations in classifying certain butterfly families. The experiment highlights the importance of informative features, careful preprocessing, model selection, and evaluation on unseen data.

## Limitations and Future Improvements

- Investigate additional biological traits that may improve classification.
- Explore alternative models and more extensive hyperparameter tuning.
- Address class-wise performance differences and investigate class imbalance.
- Evaluate feature importance and consider additional validation strategies.

## Acknowledgements

Dataset: [LepTraits — Ries Lab, Justus Liebig University Giessen](https://github.com/RiesLabGU/LepTraits)

