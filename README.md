# Butterfly Family Classification Using Machine Learning

## 1. Project Overview
This project uses machine learning to classify butterflies into six families based on their recorded biological traits. Two classification algorithms, Decision Tree and K-Nearest Neighbors (KNN), are implemented and compared.

## 2. Dataset
- **Dataset:** LepTraits – Consensus Dataset
- **Source:** [LepTraits GitHub Repository](https://github.com/RiesLabGU/LepTraits)
- **Raw dataset:** [consensus.csv](https://raw.githubusercontent.com/RiesLabGU/LepTraits/main/consensus/consensus.csv)
- **Size:** 12,448 records and 43 columns
- **Target variable:** `Family`

The six families are Hesperiidae, Lycaenidae, Nymphalidae, Papilionidae, Pieridae, and Riodinidae.

## 3. Technologies Used
- Python
- Pandas
- Scikit-learn
- Matplotlib
- Google Colab

## 4. Setup Instructions
1. Download or clone this repository.
2. Open the Jupyter Notebook (`.ipynb`) in Google Colab or Jupyter Notebook.
3. Install the required libraries if they are not already available:
   ```bash
   pip install pandas scikit-learn matplotlib
   ```
4. Run the notebook cells in order. The dataset is loaded directly from the raw GitHub link.

## 5. Results

| Model | Test Accuracy |
|---|---:|
| Decision Tree | 39.72% |
| K-Nearest Neighbors (KNN) | 44.06% |

KNN achieved higher test accuracy in this experiment. Confusion matrices and classification reports were used to evaluate model performance.

## 6. Conclusion
The project demonstrates how Decision Tree and KNN algorithms can classify butterfly families using biological trait data. KNN performed better on the test set, although both models showed varying performance across the six classes. Future improvements could include feature selection, additional preprocessing, and testing other classification algorithms.

