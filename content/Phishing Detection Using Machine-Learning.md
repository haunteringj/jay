## **Overview**  
The following note is a heavily summaried paper of my submitted phishing detection project.

This project aims to develop a **machine-learning model** to detect phishing domains by analysing its characteristics. It includes:  
- **Research** into phishing domain construction
- **Implementation** of a Random Forest Classifier  
- **Results** demonstrating high accuracy in identifying malicious domains  
- A **poster presentation** and a **Python-based solution**  

---

## **Key Components**

### 1. **Problem Statement**  
Phishing attacks becoming increasingly prevalent, with billions of hoax emails sent daily. This project explores the **automated detection** of phishing URLs using **Machine Learning (ML)** to address the limitations of heuristic and rule-based methods.

---

### 2. **Research Insights**  
Phishing URLs often exhibit traits such as:  
- Use of **IP addresses** or URL shortening  
- Verbose structures (e.g., long URLs, hyphenated domains)  
- Low traffic, **poor DNS records**, and a **young domain age**  

Machine learning techniques like **Random Forests** and **Support Vector Machines** are explored for classification accuracy.  

---

### 3. **Methodology**  
- **Data Collection**:  
  - **Phishing domains** from public repositories ([Phishing.Database](https://github.com/mitchellkrogza/Phishing.Database))  
  - **Legitimate domains** from verified internet libraries  
- **Model Development**:  
  - **Supervised Random Forest Classifier** implemented using `scikit-learn` and `Pandas`  
- **Testing and Results**:  
  - Model trained and tested with an imbalanced dataset (higher phishing links)  
  - Focus on precision, recall, and F1-score to assess accuracy  

---

### 4. **Results**  
**Classification Performance**:  
| Class           | Precision | Recall | F1-Score | Support |  
|-----------------|-----------|--------|----------|---------|  
| **Legitimate**  | 0.97      | 0.99   | 0.98     | 629     |  
| **Phishing**    | 1.00      | 1.00   | 1.00     | 5566    |  

- **Accuracy**: 99.5%  
- **Confusion Matrix**: Highlighted dataset bias (9 phishing links for every 1 legitimate link).  

---

### 5. **Challenges & Solutions**  
- **Initial Lack of ML Knowledge**: Resolved through extensive research on phishing detection methods.  
- **Dataset Imbalance**: Addressed by focusing on robust data collection and result analysis.  
- **Biases**: Noticed issues with domain suffixes (e.g., `.au`), leading to false negatives.  

---

## **Files Included**  
1. **[Full Project Report](#)**  
   Detailed explanation of the research, methodology, and results.  
2. **[Research Findings](#)**  
   In-depth study on phishing domain construction and ML approaches.  
3. **[SecEdu Poster](#)**  
   A concise, visual summary of the project, ideal for presentations.  
4. **Python Solution**:  
   - A **playable demo** where users input domains to test phishing detection.  
   - Implements a Random Forest Classifier with pre-trained datasets.  

---

## **Conclusion & Future Work**  
The project successfully demonstrates **ML-based phishing detection** as a scalable solution for cyber security.  
Future improvements:  
- Removing **domain suffix biases**  
- Implementing **hybrid ML approaches** for higher precision  

---

## **Output Example**  

**Sample Code Output**:  
```python
Input domain: suspiciouslink.com  
Prediction: Phishing 🚨  

Input domain: securebank.com.au  
Prediction: Legitimate ✅  
```

---

## **Poster Preview**  
![Project Poster](./assets/phishing_poster.png)  

---