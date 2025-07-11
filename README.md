# 🚦 Traffic Pattern Analysis Using GPS Data

## 📌 Objective

Urban areas suffer from traffic congestion due to poor understanding of traffic patterns. This project aims to analyze real-time vehicle GPS data to:

- Identify **peak traffic periods**
- Visualize **congestion-prone areas**
- Suggest better **route planning**
- Train an **ML model** to predict peak hour activity

## 📁 Dataset Description

### 🔗 Source:
**[VED (Vehicle Energy Dataset)](https://github.com/gsoh/VED)**  

### 📄 Files Used:
- Sampled from `VED_171101_week.csv` (≈ 5 lakh rows)


## 📊 Analysis & Visualizations

### 📍 1. Vehicle Count Per Hour
- Bar plot showing number of data points across 24 hours
- Helps identify **peak traffic periods** (e.g., 8–9 AM, 5–6 PM)

### 🚗 2. Speed Distribution by Hour
- Boxplots of speed by hour
- Used to highlight **congestion trends** and speed variance
- congested point per hour

### 🌍 3. Congestion Mapping
- Defined congestion as `speed < 10 km/h`
- Plotted **heatmap using latitude and longitude**
- Reveals high-density, slow-speed zones ideal for route improvements

### 📅 4. Weekday Traffic Trends
- vehicle count by day of week
- Traffic patterns analyzed across weekdays
- Helps city planners schedule work around peak days

## 🤖 ML Model: Peak Hour Prediction

### 🔍 Goal:
Classify whether a GPS datapoint is from a **peak hour** (7–9 AM or 5–7 PM)

### 📦 Features Used:
- `lat`, `lon`, `speed`, `hour`

### 🧠 Model:
- **Random Forest Classifier**
- Achieved good precision/recall for peak vs non-peak classification

### 📈 Insights:
- Feature importance: **hour** and **speed** had highest impact
- Can be extended to forecast traffic surges



## 📌 Key Insights for City Planning

- **Congestion occurs primarily in afternoon and evening**
- **Specific zones** showed repeated low-speed travel (indicating delays)
- **ML-based prediction** can help design **adaptive traffic routing systems**


## 🧾 Project Structure

```
traffic-analysis/
│
├── VED_171101_week.csv        # Raw VED dataset (1 week)(CSV)
├── Traffic.ipynb              # full code                 
├── outputs/                   # Graphs & heatmaps screnshots
├── congestion_heatmap.html    # GPS heatmap (interactive)
└── README.md                  # Project overview
```
