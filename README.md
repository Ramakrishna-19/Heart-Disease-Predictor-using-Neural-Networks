Heart-Disease-Predictor
Heart Disease Predictor using Neural Networks

This project is a machine learning application that predicts the likelihood of heart disease in individuals using clinical and lifestyle data. It leverages a Neural Network model to learn patterns in structured health data and make accurate predictions.

🚀 Features
Binary Classification: Predicts presence (Yes) or absence (No) of heart disease.
Structured Feature Processing: Works with both numerical and categorical health data.
Neural Network Architecture: Built using input, hidden, and output layers.
Trained on Real-World Dataset: Health data with over 20 features.
Real-Time Prediction Support: Make predictions from user inputs.
Robust Evaluation: Includes metrics like accuracy, precision, recall, F1-score.
🧠 How It Works
📌 Data Collection
Uses a dataset with patient information:

Age, Gender, Blood Pressure, Cholesterol, Diabetes, BMI, Smoking, Stress, Sleep Hours, etc.
Target column: Heart Disease Status (Yes or No)
🔧 Preprocessing
Handle missing values (e.g., using mean/mode imputation).
Encode categorical features using LabelEncoder or OneHotEncoder.
Scale numerical features using StandardScaler.
🧱 Model Architecture
Input Layer: Receives 20+ features.
Hidden Layers: Learn complex medical interactions.
Output Layer: Outputs probability of heart disease (0 to 1).
Activation Functions: ReLU for hidden layers, Sigmoid for output.
🏋️ Training
Loss Function: Binary Cross-Entropy
Optimizer: Adam
Epochs: Typically 50–100
Batch Size: 32 or 64
📊 Evaluation
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
ROC-AUC Score
🔮 Prediction
You can input a new patient profile for real-time prediction:

sample = {
    "Age": 60,
    "Gender": "Male",
    "Blood Pressure": 145,
    "Cholesterol Level": 240,
    "Smoking": "Yes",
    ...
}

processed_input = preprocess(sample)
prediction = model.predict(processed_input)

print("Likely Heart Disease" if prediction > 0.5 else "Low Risk")
