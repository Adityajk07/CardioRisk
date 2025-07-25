# Cardiovascular Distress Prediction using Multimodal Signal Integration
## 📄 License

This project is licensed under the [MIT License](LICENSE).



## 🩺 Project Overview

This project presents a robust machine learning pipeline to predict **high-risk cardiovascular distress** based on physiological signal data (ECG, PPG, LDF). In the absence of labeled real-world data, we implement a **semi-supervised approach** by detecting outliers (potential high-risk samples) using an **ensemble of anomaly detection algorithms**. The final model is optimized using feature selection and evaluated via cross-validation.

An interactive **Gradio-based GUI** demonstrates the end-to-end system — from signal upload to real-time risk prediction.

---

## 🎯 Objectives

- Build a label-free cardiovascular risk prediction system.
- Use **ensemble anomaly detection (LOF, iForest, One-Class SVM)** for unsupervised labeling.
- Apply **Optuna-based feature selection** for improved performance and interpretability.
- Train a supervised classifier (**Random Forest**) on generated labels.
- Provide a real-time demo using a **FastAPI + Gradio web app**.

---

## 🧠 Methodology

### 📁 1. Data
- Public and synthetic data sources (ECG, PPG, and synthetic LDF) mimicking physiological stress conditions.
- Total participants: 47
- Preprocessed using NeuroKit2 and custom denoising.

### ⚙️ 2. Signal Processing
- NeuroKit2 used for ECG/PPG feature extraction (e.g., HRV, pulse amplitude).
- Custom logic used for LDF features simulating microvascular dynamics.
- Features normalized using **StandardScaler**.

### 🤖 3. Unsupervised Risk Labeling
- Combined predictions from:
  - ✅ **Isolation Forest**
  - ✅ **Local Outlier Factor**
  - ✅ **One-Class SVM**
- Majority voting used to assign `High Risk` or `Low Risk` labels.

### 🧬 4. Feature Selection
- Applied **Optuna** to optimize:
  - Number of features
  - Random Forest hyperparameters (n_estimators, max_depth, min_samples_split)
- Final model trained on **top 48 features**.

### 🧪 5. Classification
- Final model: **Random Forest Classifier**
- Train-Test split: 80–20
- Evaluation Metrics:
  - Accuracy: **0.90**
  - Precision: **0.89**
  - Recall: **1.00**
  - F1 Score: **0.944**
  - ROC-AUC: **0.921**

---

## 6. 🛠️ Tech Stack

**Languages & Libraries**  
- Python 3.10  
- NumPy, Pandas  
- Scikit-learn  
- NeuroKit2  
- Optuna   
- Gradio    
- Matplotlib / Seaborn (for visualization)

**Tools & Platforms**  
- Google Colab (for training and experimentation)  
- GitHub (version control and documentation)  
- Google Drive (model & scaler storage)  
- VS Code (local development)

---

## 7. 📬 Contact

**Aditya J. Krishnan**  
📧 Email: adityajk07@gmail.com 
🔗 GitHub: [@Adityajk07](https://github.com/Adityajk07)  
🌐 LinkedIn: [Aditya J. Krishnan](https://www.linkedin.com/in/aditya-jk-5a89a0359)  

Feel free to reach out for collaborations, feedback, or questions related to this project!

---


