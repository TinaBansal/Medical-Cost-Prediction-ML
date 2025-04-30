
# 🏥 Medical Cost Prediction Model

This project predicts **medical insurance charges** based on personal attributes like age, BMI, smoking habits, and more. It’s a practical application of **supervised machine learning** using Python and linear regression.

Whether you're a student, data analyst, or developer, this project can help you understand the end-to-end process of building a predictive model, from loading the dataset to evaluating results.

---

## 📌 Table of Contents

- [Project Objective](#project-objective)  
- [Dataset Information](#dataset-information)  
- [Features Used](#features-used)  
- [Project Workflow](#project-workflow)  
- [Step-by-Step Installation Guide](#step-by-step-installation-guide)  
- [How to Run the Project](#how-to-run-the-project)  
- [Model Performance](#model-performance)  
- [Example Prediction](#example-prediction)  
- [Next Steps](#next-steps)  

---

## 🎯 Project Objective

To develop a machine learning model that predicts the medical insurance charges of individuals based on key factors such as age, sex, BMI, smoking status, and region.

This can be useful for:

- Health insurance companies to price plans
- Health analysts studying cost trends
- Educators teaching regression models

---

## 📊 Dataset Information

- **Source**: Kaggle’s [Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **File Name**: `insurance.csv`
- **Records**: 1,338 individuals
- **Target Variable**: `charges` (individual medical cost billed by health insurance)

---

## 🧾 Features Used

| Feature | Description |
|--------|-------------|
| `age` | Age of the individual |
| `sex` | Gender (male/female) |
| `bmi` | Body Mass Index (weight/height²) |
| `children` | Number of dependents |
| `smoker` | Smoking habit (yes/no) |
| `region` | Residential area in the US (northeast, southeast, southwest, northwest) |
| `charges` | **(Target)** Annual medical cost in USD |

---

## ⚙️ Project Workflow

1. **Data Loading** – Read CSV using `pandas`
2. **Exploratory Data Analysis (EDA)** – Visualize features with `seaborn` & `matplotlib`
3. **Preprocessing**:
   - Convert categorical values using `get_dummies()` (one-hot encoding)
   - Check for null values
4. **Modeling** – Train a **Linear Regression** model from `sklearn`
5. **Evaluation** – Use metrics like MAE, RMSE, and R² Score
6. **Prediction** – Use trained model to predict on test data

---

## 💻 Step-by-Step Installation Guide

Follow these steps to run the project on your local computer:

### ✅ 1. Prerequisites

You must have:

- Python 3.7+
- `pip` (Python package installer)
- Internet connection to download packages

### ✅ 2. Clone or Download the Project

```bash
git clone https://github.com/your-username/medical-cost-prediction.git
cd medical-cost-prediction
```

Or manually download the `.ipynb` file and place it in a folder.

### ✅ 3. Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate     # Mac/Linux
venv\Scripts\activate        # Windows
```

### ✅ 4. Install Required Packages

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### ✅ 5. Download the Dataset

- Go to [Kaggle Dataset Link](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- Download `insurance.csv`
- Place it in the same folder as the notebook OR update the path in the code.

---

## 🚀 How to Run the Project

### Option 1: Using Jupyter Notebook

1. Open terminal or Anaconda Prompt
2. Launch Jupyter:

```bash
jupyter notebook
```

3. Open `medical-cost-prediction-model.ipynb`
4. Run each cell step-by-step (Shift + Enter)

---

### Option 2: Using VS Code with Python Extension

1. Open the folder in VS Code
2. Install the **Python** extension (if not already installed)
3. Right-click the notebook and select “Run All” or “Run in Interactive Window”

---

## 📈 Model Performance

After training, the model gives the following metrics (example output):

```text
Mean Absolute Error (MAE)       : 4186.6
Mean Squared Error (MSE)        : 28715017.1
Root Mean Squared Error (RMSE)  : 5358.7
R^2 Score                       : 0.79
```

---

## 🔮 Example Prediction

Once the model is trained, you can predict charges like this:

```python
example = pd.DataFrame({
    'age': [40],
    'bmi': [30.0],
    'children': [2],
    'sex_male': [1],
    'smoker_yes': [0],
    'region_southeast': [0],
    'region_southwest': [1],
    'region_northeast': [0]
})

predicted_charge = model.predict(example)
print(f"Predicted Medical Cost: ${predicted_charge[0]:.2f}")
```

---

## 🔄 Next Steps

- Add other ML models (Random Forest, XGBoost)
- Deploy as a Streamlit app for web-based predictions
- Add hyperparameter tuning with GridSearchCV
- Use cross-validation for better generalization

---

## 📬 Contact

Feel free to open issues or contribute to improvements. If you'd like help turning this into a web app or publishing to GitHub, just ask!
