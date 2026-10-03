# 🌸 Iris Flower Classification

A machine learning classification project developed as part of the **CodeAlpha Data Science Internship**.

The objective of this project is to classify Iris flowers into three species — **Iris-setosa, Iris-versicolor, and Iris-virginica** — using their sepal and petal measurements.

## 🎯 Project Objective

Build and evaluate a machine learning classification model that predicts the species of an Iris flower from:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

## 📊 Dataset

The project uses the Iris dataset provided for the CodeAlpha task.

- **Total samples:** 150
- **Number of species:** 3
- **Samples per species:** 50
- **Features used:** 4
- **Missing values:** None

The dataset contains the following columns:

| Column | Description |
|---|---|
| `Id` | Unique identifier for each sample |
| `SepalLengthCm` | Sepal length in centimeters |
| `SepalWidthCm` | Sepal width in centimeters |
| `PetalLengthCm` | Petal length in centimeters |
| `PetalWidthCm` | Petal width in centimeters |
| `Species` | Target species |

The `Id` column is not used for model training because it is only an identifier.

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab / Jupyter Notebook

## 🔄 Project Workflow

1. Load the Iris dataset
2. Inspect the dataset structure
3. Check for missing values
4. Generate statistical summaries
5. Perform exploratory data analysis (EDA)
6. Visualize species distribution
7. Analyze feature relationships using a pairplot
8. Analyze feature correlations using a heatmap
9. Separate features and target
10. Split the data into training and testing sets
11. Standardize the numerical features
12. Train a Logistic Regression classifier
13. Generate predictions on the test set
14. Evaluate model performance
15. Analyze the confusion matrix

## 📈 Exploratory Data Analysis

The analysis showed that:

- The dataset is balanced, with 50 samples from each species.
- No missing values were found.
- Petal Length and Petal Width have a strong positive correlation.
- Iris-setosa forms a relatively distinct cluster in the feature visualizations.
- Iris-versicolor and Iris-virginica show some overlap, particularly in certain measurements.

## 🤖 Machine Learning Model

### Logistic Regression

A **Logistic Regression** classifier was used for the classification task.

Before training, the four numerical features were standardized using **StandardScaler**.

The dataset was divided into:

- **80% training data:** 120 samples
- **20% testing data:** 30 samples

## 📊 Model Performance

The model achieved:

**Accuracy: 93.33%**

On the 30 test samples:

- **28 samples** were classified correctly.
- **2 samples** were misclassified.
- All 10 Iris-setosa test samples were classified correctly.
- One Iris-versicolor sample was classified as Iris-virginica.
- One Iris-virginica sample was classified as Iris-versicolor.

### Confusion Matrix

| Actual / Predicted | Setosa | Versicolor | Virginica |
|---|---:|---:|---:|
| **Setosa** | 10 | 0 | 0 |
| **Versicolor** | 0 | 9 | 1 |
| **Virginica** | 0 | 1 | 9 |

## 📁 Project Structure

```
CodeAlpha_Iris_Flower_Classification/
│
├── Iris_Flower_Classification.ipynb
├── Iris.csv
├── README.md
└── requirements.txt
```

> **Note:** The notebook expects `Iris.csv` to be available in the same working directory.

## ▶️ How to Run

### Option 1 — Google Colab

1. Open `Iris_Flower_Classification.ipynb` in Google Colab.
2. Upload `Iris.csv` to the Colab session.
3. Run the notebook cells from top to bottom.

### Option 2 — Local Jupyter Notebook

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open:

```bash
jupyter notebook Iris_Flower_Classification.ipynb
```

Make sure `Iris.csv` is in the same directory as the notebook.

## 🏁 Conclusion

This project demonstrates a complete machine learning classification workflow, from data inspection and exploratory analysis to model training and evaluation.

The Logistic Regression model achieved **93.33% accuracy** on the unseen test dataset. The results also show that petal measurements provide useful information for distinguishing the three Iris species.

## 👨‍💻 Internship Project

**Program:** CodeAlpha Data Science Internship  
**Task:** Iris Flower Classification  
**Repository:** CodeAlpha_Iris_Flower_Classification
