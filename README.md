# 🎬 Hollywood Movie Success Prediction

> A supervised machine learning project that predicts whether a Hollywood movie will succeed at the box office — before it even releases.
> 
---

## 📌 Overview

This project uses real data from **64 Hollywood films (2022–2024)** to train a classification model that predicts movie success based on features like budget, genre, director experience, and release season.

The goal is to answer one key question:

> **What factors determine whether a movie succeeds or fails at the box office?**

---

## 📁 Project Structure

```
hollywood-movie-prediction/
│
├── data/
│   └── Data.csv   # Dataset (64 real movies)
│
├── notebooks/
│   └── movie_prediction.ipynb           # Main Jupyter Notebook
│
├── README.md
└── requirements.txt
```

---

## 📊 Dataset

The dataset contains **64 real Hollywood movies** (32 successful, 32 unsuccessful) with the following features:

| Feature | Description |
|---|---|
| `title` | Movie title |
| `year` | Release year (2022–2024) |
| `budget_million` | Production budget (USD millions) |
| `worldwide_gross_million` | Worldwide box office revenue |
| `genre` | Movie genre (Action, Drama, SciFi, etc.) |
| `director_experience` | Director experience score (1–10) |
| `runtime_min` | Movie duration in minutes |
| `release_season` | Season of release (Spring/Summer/Fall/Winter) |
| `sequel` | Whether the movie is a sequel (0 or 1) |
| `success` | **Target variable** — 1 = Success, 0 = Failure |

**Examples of movies included:**

- ✅ Successful: Barbie, Top Gun: Maverick, Oppenheimer, Inside Out 2
- ❌ Failed: Joker: Folie à Deux, The Flash, Morbius, Borderlands

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/hollywood-movie-prediction.git
cd hollywood-movie-prediction
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook notebooks/movie_prediction.ipynb
```

| Metric | Score |
|--------|-------|
| ROC-AUC | 0.66 |
| Recall  | 0.33 |
| Accuracy | 0.80 |
| Precision | 1.0 |


---

## 🧪 Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

---

## 🔬 Project Steps

### Step 1 — Load & Explore Data (EDA)
Read the CSV and get a feel for the data. Check for missing values, see the distribution of successful vs. failed movies, and explore relationships between features.

### Step 2 — Visualize
Plot charts to understand patterns. For example:
- Do bigger budgets lead to success?
- Which genres succeed more often?
- Does release season matter?

### Step 3 — Preprocessing
Convert text columns like genre and release_season into numbers using **One-Hot Encoding**, and scale numerical features.

### Step 4 — Split Data
Separate features (X) from the target (y), then split into training and test sets with an 80/20 ratio.

### Step 5 — Train Model
Train a **Random Forest Classifier** on the training data.

### Step 6 — Evaluate
Check how well the model performs on unseen data using Accuracy, F1-Score, and Confusion Matrix.

### Step 7 — Feature Importance
Find out which features matter most — is it budget, genre, director experience, or something else?

---

## 📈 Expected Results

After training, you should be able to answer:

- Is **budget** the most important factor, or is **director experience** more critical?
- Does being a **sequel** increase chances of success?
- Which **genre** has the highest success rate?
- Does **release season** (Summer vs. Winter) make a difference?

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👤 Author

**Your Name**
- GitHub: [@your-username](https://github.com/your-username)
