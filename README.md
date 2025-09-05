# ❤️ Heart Disease Predictor using Neural Networks

This project is a **machine learning application** that predicts the likelihood of heart disease in individuals using **clinical and lifestyle data**.  
It leverages a **Neural Network model** to learn patterns in structured health data and make accurate predictions.

---

## 🚀 Features
- **Binary Classification**: Predicts presence (**Yes**) or absence (**No**) of heart disease.  
- **Structured Feature Processing**: Works with both numerical and categorical health data.  
- **Neural Network Architecture**: Input, hidden, and output layers with activation functions.  
- **Trained on Real-World Dataset**: Health data with 20+ features.  
- **Real-Time Prediction Support**: Make predictions from user inputs.  
- **Robust Evaluation**: Includes metrics like accuracy, precision, recall, F1-score, ROC-AUC.  

---

## 🧠 How It Works

### 📌 Data Collection
The dataset contains patient information such as:
- **Age, Gender, Blood Pressure, Cholesterol, Diabetes, BMI, Smoking, Stress, Sleep Hours, etc.**  
- **Target column**: Heart Disease Status (`Yes` or `No`).  

### 🔧 Preprocessing
- Handle missing values (mean/mode imputation).  
- Encode categorical features (LabelEncoder / OneHotEncoder).  
- Scale numerical features (StandardScaler).  

### 🧱 Model Architecture
- **Input Layer**: 20+ features.  
- **Hidden Layers**: Capture complex medical interactions.  
- **Output Layer**: Sigmoid activation → probability (0 to 1).  
- **Activation Functions**: ReLU for hidden layers, Sigmoid for output.  

### 🏋️ Training
- **Loss Function**: Binary Cross-Entropy  
- **Optimizer**: Adam  
- **Epochs**: 50–100  
- **Batch Size**: 32 or 64  

### 📊 Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix  
- ROC-AUC Score  

---

## 🔮 Prediction Example

```python
sample = {
    "Age": 60,
    "Gender": "Male",
    "Blood Pressure": 145,
    "Cholesterol Level": 240,
    "Smoking": "Yes",
    "Diabetes": "No",
    "BMI": 28.5,
    "Stress": "High",
    "Sleep Hours": 6
}

processed_input = preprocess(sample)
prediction = model.predict(processed_input)

print("Likely Heart Disease" if prediction > 0.5 else "Low Risk")
