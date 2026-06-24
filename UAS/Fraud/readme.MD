# Machine Learning Fraud Detection - Final Term

## Data Diri

| Kategori | Detail |
| :--- | :--- |
| **Nama** | **Febrio Bagus Budianda** |
| **Kelas** | **TK-46-GAB** |
| **NIM** | **1103223223** |

---

##  Problem Statement

Fraud detection merupakan masalah klasifikasi dengan karakteristik utama:
- **Class imbalance tinggi** (fraud sangat sedikit dibanding non-fraud)
- **Cost-sensitive problem** (kesalahan deteksi fraud jauh lebih mahal)
- **Pattern yang kompleks & non-linear**

Tujuan proyek ini bukan sekadar membuat model akurat, tetapi:
**Mendeteksi fraud secara reliable dengan meminimalkan False Negative**

---

##  Pendekatan yang Digunakan

Pipeline yang dibangun bersifat **end-to-end machine learning workflow**, mencakup:

1. Data Understanding  
2. Data Preparation  
3. Modeling  
4. Optimization  
5. Evaluation  
6. Experiment Tracking  

Tools utama:
- **MLflow** → tracking eksperimen & reproducibility  
- **Optuna** → hyperparameter optimization  

---

##  Exploratory Data Analysis (EDA)

Analisis awal menunjukkan:

- Dataset sangat **imbalanced (~96.5% non-fraud)**  
- Distribusi fitur menunjukkan adanya pola tertentu namun tidak linear  
- Korelasi antar fitur relatif rendah → model non-linear lebih cocok  

Insight:
Model sederhana tanpa handling imbalance hampir pasti bias ke kelas mayoritas.

---

##  Data Preprocessing Strategy

Langkah preprocessing tidak hanya teknis, tapi strategis:

### 1. Missing Value Handling
- Drop fitur dengan missing value tinggi (>50%)
- Menghindari noise dan informasi yang tidak stabil

### 2. Feature Selection
- Menghapus fitur tidak relevan
- Mengurangi dimensionality → mencegah overfitting

### 3. Encoding
- Transformasi variabel kategorikal → numerik

Insight:
Preprocessing menentukan **batas performa maksimal model**.

---

##  Data Splitting Strategy

Dataset dibagi menjadi:
- Training Set
- Testing Set

Prinsip utama:
**No data leakage**

Jika leakage terjadi → hasil evaluasi menjadi tidak valid (over-optimistic).

---

## Hyperparameter Optimization (Optuna)

Alih-alih manual tuning, digunakan **Optuna** karena:

- Efficient search (Bayesian Optimization)
- Mencari kombinasi optimal secara adaptif
- Lebih cepat dibanding grid/random search

Contoh parameter yang dioptimasi:
- learning_rate
- depth
- n_estimators

Insight:
Hyperparameter tuning sering memberi impact lebih besar dibanding ganti model.

---

##  Experiment Tracking (MLflow)

MLflow digunakan untuk:
- Logging parameter
- Tracking metric (AUC, F1, dll)
- Menyimpan model

Tujuan:
**Reproducibility & comparison antar eksperimen**

Tanpa tracking → eksperimen tidak bisa divalidasi ulang.

---

##  Model Training

Model dilatih menggunakan hasil tuning terbaik.

Karakteristik model:
- Mampu menangkap pola non-linear
- Robust terhadap noise
- Cocok untuk tabular data

---

## Evaluation Strategy

Evaluasi TIDAK hanya pakai accuracy.

Metric utama:
- **Recall (Fraud Class)** → PRIORITAS
- **Precision**
- **F1-Score**
- **AUC-ROC**
- **Confusion Matrix**

### Fokus Utama:
**Minimizing False Negative**

Karena:
- False Negative = fraud lolos → kerugian nyata

Insight:
Model “akurasi tinggi” bisa jadi useless di fraud detection.

---

## Key Insights

- Imbalanced dataset adalah core challenge
- Accuracy = misleading metric
- Recall lebih penting dari precision (dalam konteks fraud)
- Hyperparameter tuning + tracking = game changer
- Pipeline lebih penting daripada model tunggal

---

## Kesimpulan

Model Machine Learning dapat digunakan untuk fraud detection dengan baik jika:

- Data diproses dengan benar
- Imbalance ditangani dengan serius
- Evaluasi menggunakan metric yang tepat
- Eksperimen dilakukan secara sistematis

Tanpa itu semua:
 Model hanya terlihat bagus di atas kertas, tapi gagal di dunia nyata.

---

## Cara Menjalankan

1. Buka `FraudDetection.ipynb`
2. Jalankan semua cell secara berurutan
3. Pastikan dependency terinstall:
   - pandas
   - numpy
   - scikit-learn
   - mlflow
   - optuna


