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
**Image to add:** `images/venue_distribution.png`  
(Bar chart showing number of matches per venue)

![Venue Distribution](images/venue_distribution.png)

---

### 🏏 Top Batsmen by Total Runs
**Image to add:** `images/top_batsmen.png`  
(Top 10 batsmen by total runs)

![Top Batsmen](images/top_batsmen.png)

---

### 🎯 Top Bowlers by Total Wickets
**Image to add:** `images/top_bowlers.png`  
(Top 10 bowlers by total wickets)

![Top Bowlers](images/top_bowlers.png)

---

### 🔗 Feature Correlation Heatmap
**Image to add:** `images/correlation_heatmap.png`  
(Heatmap showing correlation between numerical features)

![Correlation Heatmap](images/correlation_heatmap.png)

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
**Image to add:** `images/training_loss_curve.png`  
(Line plot showing loss convergence)

![Training Loss Curve](images/training_loss_curve.png)

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
**Image to add:** `images/widget_output.png`  
(Screenshot showing predicted total score)

![Widget Output](images/widget_output.png)

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Karunakar24/Cricket-League-Score-Prediction.git
cd Cricket-League-Score-Prediction
