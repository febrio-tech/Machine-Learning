# 🎵 Midterm Machine Learning — Song Release Year Prediction (Regression)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-orange)
![MLFlow](https://img.shields.io/badge/MLFlow-Tracking-green)
![Optuna](https://img.shields.io/badge/Optuna-Tuning-purple)

---

## 📌 Tujuan Proyek

Membangun pipeline regresi end-to-end untuk **memprediksi tahun rilis lagu** berdasarkan fitur audio menggunakan algoritma machine learning.

---

## 📂 Struktur Repository

```
midterm-machine-learning/
│
├── midterm_regresi.ipynb       # Notebook utama (pipeline lengkap)
├── midterm-regresi-dataset.csv # Dataset (515.345 lagu, 90 fitur audio)
├── mlruns/                     # MLFlow experiment logs
│   └── ...
├── *.png                       # Visualisasi & grafik output
└── README.md                   # Dokumentasi ini
```

---

## 📊 Dataset

| Properti       | Detail                                 |
|----------------|----------------------------------------|
| Nama File      | `midterm-regresi-dataset.csv`          |
| Jumlah Baris   | 515.345 lagu                           |
| Jumlah Kolom   | 91 (1 target + 90 fitur audio)         |
| Target         | Tahun rilis lagu (1922–2011)           |
| Fitur          | Numerik (timbre & audio characteristics) |
| Missing Values | Tidak ada                              |

> Kolom pertama adalah **tahun rilis** (target label), kolom lainnya adalah `feature_1` hingga `feature_90` yang merepresentasikan karakteristik audio.

---

## 🔄 Alur Pipeline

```
Data Loading
    ↓
EDA (Distribusi, Korelasi, Outlier)
    ↓
Preprocessing (Outlier Capping, Train-Test Split, StandardScaler)
    ↓
Feature Selection (SelectKBest — Top 50 Fitur)
    ↓
Model Training (Linear Regression, Ridge, Random Forest, Gradient Boosting)
    ↓
Hyperparameter Tuning (Optuna — 20 trials)
    ↓
Evaluasi (MSE, RMSE, MAE, R²)
    ↓
Interpretasi (LIME)
    ↓
Experiment Tracking (MLFlow)
```

---

## 🤖 Model yang Digunakan

| Model | Keterangan |
|-------|-----------|
| **Linear Regression** | Baseline sederhana |
| **Ridge Regression** | Linear dengan L2 regularization |
| **Random Forest** | Ensemble berbasis decision tree |
| **Gradient Boosting** | Boosting ensemble |
| **Random Forest + Optuna** | Model terbaik setelah tuning |

---

## 📈 Hasil & Metrik Evaluasi

| Model | RMSE ↓ | MAE ↓ | R² ↑ |
|-------|--------|-------|------|
| Linear Regression | ~9.x | ~7.x | ~0.2x |
| Ridge Regression | ~9.x | ~7.x | ~0.2x |
| Random Forest | ~7.x | ~5.x | ~0.4x |
| Gradient Boosting | ~8.x | ~6.x | ~0.3x |
| **RF + Optuna (Best)** | **~6.x** | **~5.x** | **~0.5x** |

> *Nilai eksak dapat dilihat di notebook atau MLFlow dashboard*

### Penjelasan Metrik:
- **MSE** — Mean Squared Error: rata-rata kuadrat error prediksi
- **RMSE** — Root MSE: error rata-rata dalam satuan tahun
- **MAE** — Mean Absolute Error: rata-rata error absolut dalam tahun
- **R²** — Koefisien determinasi: seberapa baik model menjelaskan variansi target

---

## 🔍 Interpretasi dengan LIME

LIME (*Local Interpretable Model-agnostic Explanations*) digunakan untuk menjelaskan prediksi individual:
- Fitur **hijau** → mendorong prediksi ke tahun yang lebih baru
- Fitur **merah** → mendorong prediksi ke tahun yang lebih lama
- Panjang bar → besarnya kontribusi fitur terhadap prediksi

---

## ⚡ Hyperparameter Tuning (Optuna)

Optuna digunakan untuk mencari hyperparameter optimal pada Random Forest:

| Parameter | Search Space |
|-----------|-------------|
| `n_estimators` | 50 – 300 |
| `max_depth` | 5 – 30 |
| `min_samples_split` | 2 – 20 |
| `min_samples_leaf` | 1 – 10 |
| `max_features` | 0.3 – 1.0 |

**Jumlah trials:** 20 | **Sampler:** TPE (Tree-structured Parzen Estimator)

---

## 📡 Experiment Tracking (MLFlow)

Semua eksperimen di-log ke MLFlow:
- **Parameters:** hyperparameter model, jumlah fitur
- **Metrics:** MSE, RMSE, MAE, R²
- **Artifacts:** model tersimpan + gambar visualisasi

Jalankan dashboard MLFlow:
```bash
mlflow ui
# Buka browser: http://localhost:5000
```

---

## 🚀 Cara Menjalankan

1. **Clone repository:**
```bash
git clone https://github.com/<username>/midterm-machine-learning.git
cd midterm-machine-learning
```

2. **Install dependencies:**
```bash
pip install scikit-learn optuna mlflow lime pandas numpy matplotlib seaborn
```

3. **Pastikan dataset ada di folder yang sama:**
```
midterm-regresi-dataset.csv
```

4. **Jalankan notebook:**
```bash
jupyter notebook midterm_regresi.ipynb
```

5. **Lihat MLFlow dashboard:**
```bash
mlflow ui
```

---

## 🛠️ Dependencies

```
scikit-learn
optuna
mlflow
lime
pandas
numpy
matplotlib
seaborn
jupyter
```

---

## 👤 Identitas

| | |
|---|---|
| **Nama** | [Nama Kamu] |
| **NIM** | [NIM Kamu] |
| **Kelas** | [Kelas Machine Learning Kamu] |
| **Mata Kuliah** | Machine Learning |

---

## 📝 Catatan

- Dataset besar (515k+ baris) — disarankan menggunakan GPU/Colab untuk training yang lebih cepat
- Untuk hasil terbaik, coba tambahkan model XGBoost atau LightGBM
- Ubah `N_TRIALS` di Optuna untuk eksplorasi lebih dalam
