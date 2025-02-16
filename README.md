# **Cybersecurity Intrusion Detection Using Ensemble Methods**

## **Overview**
  In today's digital landscape, cyber threats continue to evolve, posing significant risks to data security and network integrity. This project focuses on developing an Intrusion Detection System (IDS) using machine learning, specifically ensemble learning techniques, to identify malicious activities based on network traffic and user behavior patterns.

## **Dataset**
  The dataset contains a combination of network-based and user behavior-based features, including:
  - Network-Based Features:
      - network_packet_size: Packet size (64–1500 bytes), useful for identifying abnormal traffic.
      - protocol_type: Communication protocol (TCP, UDP, ICMP) to analyze traffic patterns.
      - encryption_used: Encryption type (AES, DES, None), indicating security levels in communication.
  - User Behavior-Based Features:
      - login_attempts: Number of login attempts, useful for detecting brute-force attacks.
      - session_duration: Length of user sessions, where unusually long durations may indicate unauthorized access.
      - failed_logins: Failed login attempts, which could suggest credential stuffing or dictionary attacks.
      - unusual_time_access: A binary flag for logins occurring at unusual times.
      - ip_reputation_score: A score (0–1) assessing the trustworthiness of an IP address.
      - browser_type: Browser used, where “Unknown” may indicate automated or suspicious access.
  The target variable, attack_detected, is a binary classification (1 = attack detected, 0 = normal activity).

## **Methodology**
  This project applies various ensemble learning techniques to enhance detection performance, including:
  - AdaBoost: Improves weak classifiers by sequentially adjusting model weights.
  - XGBoost & LightGBM: Gradient boosting methods optimized for speed and accuracy.
  - Random Forest: A collection of decision trees that enhances model generalization.
  To ensure optimal model performance, hyperparameter tuning is performed using RandomizedSearchCV and BayesSearchCV.

## **Results**
  The Random Forest classifier tuned via RandomizedSearchCV achieved the best performance with a macro F1-Score of 0.8805 and an accuracy of 0.89. This indicates that hyperparameter tuning improved the performance of all models, with Random Forest providing the most balanced and robust detection of cyber intrusions.

## **Future Enhancements**
  Possible improvements include:
  - Incorporating real-time threat detection capabilities.
  - Exploring deep learning models (e.g., LSTM, CNN) for sequential analysis.
  - Enhancing feature engineering to improve classification accuracy.

## **How to Use**
  ```bash
  git clone https://github.com/your-username/your-project.git
  cd your-project
  ```
