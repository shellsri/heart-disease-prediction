# 🫀 Heart Disease Prediction

A machine learning web app that predicts a user's risk of heart disease based on clinical input features. Built with a KNN classifier and deployed via Streamlit.

**🔗 Live App:** [heart-disease-prediction-gwges9rrnuatsmh9abxh36.streamlit.app](https://heart-disease-prediction-gwges9rrnuatsmh9abxh36.streamlit.app/)

---

## 📌 Overview

This app takes patient health metrics as input and uses a pre-trained **K-Nearest Neighbors (KNN)** model to predict whether the patient is at **high or low risk** of heart disease. The model was trained on a heart disease dataset and saved using `joblib` for fast inference.

---

## 🚀 Features

- Interactive web UI built with **Streamlit**
- Real-time prediction with a single click
- Accepts 11 clinical features including age, cholesterol, ECG results, and more
- Uses a pre-fitted **StandardScaler** to normalize inputs before prediction
- Displays clear ✅ / ⚠️ risk output

---

## 🧠 Model Details

| Property        | Value                        |
|-----------------|------------------------------|
| Algorithm       | K-Nearest Neighbors (KNN)    |
| Preprocessing   | StandardScaler               |
| Serialization   | joblib (`.pkl` files)        |
| Input Features  | 11 clinical variables        |
| Output          | Binary (Heart Disease: Yes/No) |

---

## 📥 Input Features

| Feature               | Type       | Description                                      |
|-----------------------|------------|--------------------------------------------------|
| Age                   | Slider     | Patient age (18–100)                            |
| Sex                   | Dropdown   | M / F                                            |
| Chest Pain Type       | Dropdown   | ATA, NAP, TA, ASY                               |
| Resting Blood Pressure| Number     | In mm Hg (80–200)                               |
| Cholesterol           | Number     | In mg/dL (100–600)                              |
| Fasting Blood Sugar   | Dropdown   | > 120 mg/dL → 1, else 0                        |
| Resting ECG           | Dropdown   | Normal, ST, LVH                                 |
| Max Heart Rate        | Slider     | 60–220 bpm                                      |
| Exercise-Induced Angina | Dropdown | Y / N                                           |
| Oldpeak (ST Depression) | Slider  | 0.0–6.0                                         |
| ST Slope              | Dropdown   | Up, Flat, Down                                  |

---

## 🗂️ Project Structure

```
heart-disease-prediction/
├── app.py              # Streamlit app
├── KNN_heart.pkl       # Trained KNN model
├── scaler.pkl          # Fitted StandardScaler
├── columns.pkl         # Expected feature column order
├── requirements.txt    # Python dependencies
└── README.md
```

---

## ⚙️ Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/shellsri/heart-disease-prediction.git
cd heart-disease-prediction
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Launch the app**
```bash
streamlit run app.py
```

The app will open at `http://localhost:8501`.

---

## 🛠️ Tech Stack

- **Python** — Core language
- **Streamlit** — Web UI framework
- **Scikit-learn** — KNN model & StandardScaler
- **Pandas** — Input data handling
- **Joblib** — Model serialization

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Built by [Shelly](https://github.com/shellsri)*
