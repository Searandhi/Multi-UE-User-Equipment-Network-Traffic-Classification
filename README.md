# 🌐 AI Multi-UE Network Traffic Classification

## 🚀 Overview
This project focuses on intelligent network traffic classification using machine learning techniques. It analyzes network flow data to accurately classify traffic into multiple application categories, including both VPN and non-VPN traffic.

The system improves network performance, security, and Quality of Service (QoS) through efficient traffic identification.

---

## 🎯 Problem Statement
- Increasing complexity of network traffic due to multiple applications  
- Difficulty in identifying traffic type, especially under VPN  
- Inefficient QoS without proper classification  
- Need for an automated and intelligent classification system  

---

## 💡 Solution
This project uses an ensemble machine learning approach to classify network traffic into 14 categories by analyzing flow-based features instead of packet content, ensuring privacy-preserving analysis.

---

## 🎯 Objectives
- Classify traffic into 14 categories  
- Detect both VPN and non-VPN traffic  
- Improve Quality of Service (QoS)  
- Optimize network resource allocation  
- Achieve high classification accuracy  

---

## 📊 Dataset Overview
- ~55,000 network flow records  
- 14 classes:
  - 7 Non-VPN traffic types  
  - 7 VPN traffic types  
- Includes applications like:
  - Browsing  
  - Chat  
  - Streaming  
  - VOIP  
  - File Transfer  

---

## 🧠 Features Used
- Flow bytes per second  
- Packet rate  
- Flow duration  
- Inter-arrival times (min, mean, std, max)  
- Forward & backward packet metrics  

👉 Privacy-preserving: No payload inspection  

---

## ⚙️ Data Processing
- Label encoding for VPN & class labels  
- Train-Test Split: 80% / 20%  
- Handling class imbalance using balanced metrics  

---

## 🔬 Feature Engineering
- Created 20 additional features  
- Total features: 33  

Types:
- Ratio-based features  
- Log transformations  
- Interaction features  

---

## 🤖 Model Architecture

### Level 0 – Base Models
- XGBoost  
- LightGBM  

### Level 1 – Meta Model
- Logistic Regression  

👉 Stacking ensemble used for final prediction  

---

## 📈 Results
- Accuracy: **97.53%**  
- Balanced Accuracy: **97.24%**  
- High Precision, Recall, and F1-score  
- Effective for both VPN & non-VPN traffic  

---

## 🌍 Impact
- Improves network performance and QoS  
- Helps in traffic monitoring and management  
- Enables efficient resource allocation  
- Useful for cybersecurity and network optimization  

---

## 🛠️ How to Run

```bash
git clone https://github.com/Searandhi/Multi-UE-User-Equipment-Network-Traffic-Classification.git
cd Multi-UE-User-Equipment-Network-Traffic-Classification
pip install -r requirements.txt
python main.py
