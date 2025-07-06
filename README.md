# 🛡️ Phish Catcher

**Client-Side Defence Against Web Spoofing Attacks Using Machine Learning**

Phish Catcher is a Google Chrome extension designed to detect and defend against phishing and web spoofing attacks in real time. Utilizing machine learning techniques—specifically the Random Forest algorithm—the tool analyzes URLs and web page features to determine their legitimacy with impressive accuracy and performance.

---

## 📌 Features

* 🌐 Detects phishing attempts in real-time while browsing
* 🧠 Uses a trained Random Forest classifier for accurate URL classification
* 🔒 Operates entirely on the client-side for privacy and independence
* 📊 Achieves **98.5% accuracy and precision** over tested URLs
* ⚙️ Compares performance with SVM and XGBoost models
* 💡 Includes Chrome extension for live URL analysis

---

## 🎯 Objective

To provide a **client-side phishing detection** system that helps users avoid falling victim to fake login pages and phishing links by analyzing web URLs using machine learning.

---

## 🛠️ Technologies Used

* **Python** (Backend and ML processing)
* **Scikit-learn, XGBoost** (Machine Learning libraries)
* **Google Chrome Extension** (for user interaction)
* **PhishTank Dataset** (for training & evaluation)
* **Random Forest, SVM, XGBoost** (Algorithms used)

---

## 🧪 Results

| Model                        | Accuracy  | Precision | Recall | F1 Score  |
| ---------------------------- | --------- | --------- | ------ | --------- |
| Support Vector Machine (SVM) | \~97%     | \~97%     | \~97%  | \~97%     |
| Random Forest (Proposed)     | **98.5%** | **98.5%** | 98.5%  | **98.5%** |
| XGBoost (Extension Model)    | \~98%     | \~98%     | 98%    | 98%       |

---

## 📂 Folder Structure

```
.
├── Dataset/
│   ├── phish_tank_storm.csv
│   └── testData.csv
├── model/
│   ├── svm.txt
│   ├── rf.txt
│   └── xgb.txt
├── processed.csv
├── extension/
│   └── manifest.json, popup.html, background.js (Chrome Extension)
├── main.py
├── README.md
```

---

## 🚀 How It Works

1. **Extract Features**: URLs are parsed for suspicious patterns (e.g., quantity of dots, slashes, special symbols, etc.).
2. **Train Models**: Random Forest is trained using the PhishTank dataset, alongside SVM and XGBoost.
3. **Prediction**: Chrome extension captures current URL and classifies it using the trained model.
4. **Visualization**: Confusion matrices and performance metrics plotted using Seaborn and Matplotlib.

---

## 📦 Installation & Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/phish-catcher.git
   cd phish-catcher
   ```

2. Install Python dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Train and evaluate:

   ```bash
   python main.py
   ```

4. Load `extension/` folder as an **unpacked extension** in Chrome to enable live detection.

---

## 🔒 Security Scope

* Analyzes structural elements of URLs (not content)
* Works independently of server-side defenses
* Designed to supplement—not replace—SSL/TLS and two-factor authentication

---

