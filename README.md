# 🏏 Cricket League Score Prediction using Deep Learning

## 📌 Project Overview
This project predicts the **final score of a cricket league innings** using **ball-by-ball IPL data (2008–2017)**.  
A **deep learning–based regression model** is used to capture the nonlinear and contextual nature of cricket matches, enabling **real-time score prediction**.

The project demonstrates an **end-to-end machine learning workflow**, from data preprocessing and exploratory analysis to model training and interactive prediction.

---

## 🎯 Problem Statement
Cricket is a highly dynamic sport where match conditions change ball by ball.  
Traditional regression techniques fail to capture these complex relationships.

**Objective:**  
> Predict the final innings score of a cricket match based on the current state of play.

---

## 📂 Dataset
- **Source:** IPL Ball-by-Ball Dataset (2008–2017)
- **Granularity:** One row per ball
- **Target Variable:** Final innings total score

### 🔑 Features Used
- Batting Team  
- Bowling Team  
- Venue  
- Batsman  
- Bowler  
- Current Runs  
- Wickets Fallen  
- Overs Completed  
- Striker Indicator  

---

## 🔍 Exploratory Data Analysis (EDA)

### 📊 Venue Distribution
<img width="1114" height="444" alt="image" src="https://github.com/user-attachments/assets/c83d625b-8fbe-4cd7-a3fb-e423ae5ee012" />


---

### 🏏 Top Batsmen by Total Runs
<img width="1094" height="551" alt="image" src="https://github.com/user-attachments/assets/364a1f1d-378b-4fba-a0f4-562054d7efd7" />

---

### 🎯 Top Bowlers by Total Wickets
<img width="1082" height="547" alt="image" src="https://github.com/user-attachments/assets/8e93c79f-aba0-49a9-8e88-f12d1fd80b55" />


---

### 🔗 Feature Correlation Heatmap
<img width="903" height="538" alt="image" src="https://github.com/user-attachments/assets/186226e6-7de2-4584-bf96-8b170c4c40a9" />


---

## ⚙️ Data Preprocessing
- Removed irrelevant identifiers (match ID, date)
- Label encoded categorical variables
- Applied **Min-Max Scaling** to numerical features
- Removed highly correlated and redundant features to reduce multicollinearity

---

## 🧠 Model Architecture
A **Deep Neural Network (DNN)** was designed to model contextual and nonlinear patterns in cricket scoring.

### 🏗 Architecture
- Input Layer: 9 features  
- Hidden Layer 1: 512 neurons (ReLU)  
- Hidden Layer 2: 216 neurons (ReLU)  
- Output Layer: 1 neuron (Linear)

### ⚙️ Training Configuration
- Loss Function: **Huber Loss**
- Optimizer: **Adam**
- Batch Size: 64
- Epochs: 10

---

### 📉 Training vs Validation Loss
<img width="547" height="421" alt="image" src="https://github.com/user-attachments/assets/64dcb7ef-a712-4c69-9587-5f5878f042b4" />


---

## 📈 Results & Evaluation
- **Evaluation Metric:** Mean Absolute Error (MAE)
- **Achieved MAE:** ~ **14 runs**
- Performance is consistent with benchmarks reported in prior cricket analytics research

The model converged within a few epochs and showed stable performance on unseen data.

---

## 🧪 Interactive Score Prediction
An interactive prediction tool was built using **ipywidgets**, allowing users to input live match details and obtain predicted final scores in real time.

### 📸 Example Prediction Output
<img width="332" height="376" alt="image" src="https://github.com/user-attachments/assets/69da627c-eec5-4998-b6a7-5caed4864501" />


---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Karunakar24/Cricket-League-Score-Prediction.git
cd Cricket-League-Score-Prediction
