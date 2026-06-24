# Machine Learning - Final Term Regresi

## Data Diri

| Kategori | Detail |
| :--- | :--- |
| **Nama** | **Febrio Bagus Budianda** |
| **Kelas** | **TK-46-GAB** |
| **NIM** | **1103223223** |

---

## 1. Tujuan Repositori

Repository ini berisi implementasi end-to-end machine learning pipeline untuk melakukan prediksi tahun rilis lagu menggunakan metode regression berbasis Machine Learning.

Proyek ini dibuat untuk project UAS Machine Learning Regresi yang berfokus pada prediksi nilai kontinu (continuous value), yaitu release year lagu, berdasarkan audio features numerik yang tersedia pada dataset.

---

## 2. Gambaran Singkat Proyek

Pada proyek ini dilakukan proses regression terhadap dataset audio features lagu untuk memprediksi tahun rilis lagu menggunakan model machine learning berbasis boosting.

Tahapan yang dilakukan dalam proyek ini meliputi:

- Data preprocessing
- Penanganan missing values
- Penanganan outliers
- Exploratory Data Analysis (EDA)
- Feature scaling
- Data splitting (train, validation, test)
- Baseline model training
- Hyperparameter tuning menggunakan Optuna
- Model evaluation
- Model interpretability menggunakan LIME
- Experiment tracking menggunakan MLflow
- Model saving

Dataset yang digunakan:
- `midterm-regresi-dataset.csv`


Link Dataset: **https://drive.google.com/file/d/13hoYuDDKTOZ4OUTZrdlaKG-OSIK_lnbU/view?usp=sharing**

---

## 3. Model

Model utama yang digunakan:
- XGBoost Regressor (GPU Accelerated)

Model tambahan guna membandingkan model XGBoost:
- RandomForestRegressor

---

## 4. Evaluation Metrics

Metode evaluasi yang digunakan:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R-squared (R²)

### Hasil Evaluasi Model

| Stage | MSE | RMSE | MAE | R² |
|---|---|---|---|---|
| RandomForestRegressor | 79.40 | 8.91 | 6.22 | 0.33 |
| XGBoost | 76.61 | 8.75 | 6.12 | 0.356 |
| XGBoost + Optuna Tuning | 72.28 | 8.50 | 5.91 | 0.393 |

Hasil evaluasi menunjukkan bahwa model XGBoost yang telah dioptimasi menggunakan Optuna menghasilkan performa terbaik dibandingkan model baseline sebelumnya.

---

## 5. Hyperparameter Tuning

Hyperparameter tuning dilakukan menggunakan framework Optuna dengan total **35** trials untuk mencari kombinasi parameter terbaik pada model XGBoost.

Beberapa parameter yang dioptimasi:
- n_estimators
- max_depth
- learning_rate
- subsample
- colsample_bytree
- gamma
- reg_alpha
- reg_lambda

---

## 6. Interpretability dan Tracking

Untuk meningkatkan interpretability model, proyek ini menggunakan:
- LIME (Local Interpretable Model-Agnostic Explanations)

Untuk tracking experiment machine learning digunakan:
- MLflow

MLflow digunakan untuk:
- Logging metrics
- Logging hyperparameters
- Logging model artifacts
- Tracking experiment runs

---

## 7. Model Saving

Model hasil training disimpan dalam format:
- `.pkl`
- `.json`
Link savemodel-tuned karena file terlalu besar berada di file `release_year_xgb_model_bundle.txt` atau https://drive.google.com/file/d/1isCcoUFoRtSE717DibrkhvkQhgi4F-Gl/view?usp=sharing

Komponen yang disimpan:
- trained model
- scaler
- feature columns
- best hyperparameters
- evaluation metrics

---

## 8. Repository Structure / Notebook Navigation

```text
UAS_ML_Regresi.ipynb
requirements.txt

savemodel-tuned/
├── release_year_xgb_model_bundle.txt
├── best_params.json
└── test_metrics.json

README.md
```

---

## 9. Conclusion

Berdasarkan hasil eksperimen yang dilakukan, model XGBoost Regressor dengan hyperparameter tuning menggunakan Optuna mampu memberikan performa terbaik dalam memprediksi tahun rilis lagu berdasarkan audio features numerik.

Model berhasil mencapai:
- MSE sebesar 72.28
- RMSE sebesar 8.50
- MAE sebesar 5.91
- R² sebesar 0.393

Hasil ini menunjukkan bahwa model mampu mempelajari pola dari audio features dengan cukup baik untuk melakukan prediksi release year lagu.

## How to Run the Project

### Clone Repository

```bash
git clone <repository-link>
cd UAS-Regresi
```

---

### Create Virtual Environment

```bash
python -m venv venv
```

---

### Activate Virtual Environment

#### Windows (PowerShell)

```bash
venv\Scripts\activate
```

#### Windows (CMD)

```bash
venv\Scripts\activate.bat
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```
