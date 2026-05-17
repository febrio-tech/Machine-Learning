# Machine-Learning
# 🛒 Midterm Machine Learning — Customer Clustering

## 👤 Identitas

| | |
|---|---|
| **Nama** | Febrio Bagus Budianda |
| **NIM** | 1103223223 |
| **Kelas** | TK-46-GAB |
| **Mata Kuliah** | Machine Learning |
| **Tugas** | UTS — End-to-End Clustering Pipeline |

---

## 1. Tujuan
Merancang dan mengimplementasikan pipeline machine learning end-to-end untuk tugas **clustering pelanggan** berdasarkan perilaku penggunaan kartu kredit.

---

## 📂 Struktur Repository

```
midterm-machine-learning-clustering/
│
├── customer_clustering_midterm.ipynb   # Notebook utama
├── README.md                           # Dokumentasi ini
└── mlruns/                             # Folder MLFlow tracking (auto-generated)
```

---

## 📊 Dataset

**Dataset:** `clusteringmidterm.csv`  
**Sumber:** Dataset kredit pelanggan (Credit Card Customer Behavior)

| Fitur | Deskripsi |
|---|---|
| CUST_ID | ID unik pelanggan |
| BALANCE | Saldo rata-rata kartu kredit |
| PURCHASES | Total pembelian |
| CASH_ADVANCE | Total penarikan tunai |
| CREDIT_LIMIT | Limit kredit |
| PAYMENTS | Total pembayaran |
| PRC_FULL_PAYMENT | Proporsi pembayaran penuh |
| TENURE | Lama kepemilikan kartu (bulan) |
| ... | (17 fitur total) |

---

## 🔧 Pipeline End-to-End

```
Raw Data
   │
   ▼
[1] EDA & Visualisasi
   │
   ▼
[2] Preprocessing
    ├── Median Imputation (missing values)
    ├── IQR Capping (outlier handling)
    └── RobustScaler (normalisasi)
   │
   ▼
[3] Feature Engineering
    ├── PAYMENT_TO_BALANCE_RATIO
    ├── CASH_ADVANCE_RATIO
    ├── AVG_PURCHASE_VALUE
    └── CREDIT_UTILIZATION
   │
   ▼
[4] Dimensionality Reduction (PCA — 90% variance)
   │
   ▼
[5] Clustering Models
    ├── K-Means       (Optuna tuning)
    ├── Hierarchical  (Ward linkage)
    └── DBSCAN        (Optuna tuning)
   │
   ▼
[6] Evaluasi
    ├── Silhouette Score
    ├── Davies-Bouldin Score
    └── Calinski-Harabasz Score
   │
   ▼
[7] Interpretasi Cluster + Visualisasi
   │
   ▼
[8] MLFlow Tracking
```

---

## 🤖 Model yang Digunakan

| Model | Hyperparameter Tuning | Keterangan |
|---|---|---|
| **K-Means** | Optuna (n_clusters, init, n_init) | Model utama |
| **Hierarchical Clustering** | Manual (Ward linkage) | Pembanding struktural |
| **DBSCAN** | Optuna (eps, min_samples) | Deteksi noise/anomali |

---

## 📈 Metrik Evaluasi

| Metrik | Arah | Keterangan |
|---|---|---|
| Silhouette Score | ↑ lebih baik | Seberapa baik data masuk ke clusternya |
| Davies-Bouldin Score | ↓ lebih baik | Rasio jarak intra vs antar cluster |
| Calinski-Harabasz Score | ↑ lebih baik | Dispersi antar cluster vs dalam cluster |

---

## 🧭 Cara Menjalankan Notebook

1. **Clone repository ini:**
   ```bash
   git clone https://github.com/USERNAME/midterm-machine-learning.git
   cd midterm-machine-learning
   ```

2. **Install dependencies:**
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn mlflow optuna scipy
   ```

3. **Siapkan dataset:**
   - Letakkan `clusteringmidterm.csv` di folder yang sama dengan notebook
   - Atau jalankan cell "OPSI B" untuk menggunakan dummy data

4. **Jalankan notebook:**
   ```bash
   jupyter notebook customer_clustering_midterm.ipynb
   ```

5. **Lihat MLFlow dashboard:**
   ```bash
   mlflow ui
   # Buka http://localhost:5000 di browser
   ```

---

## 💡 Insight Hasil Clustering

Dari hasil clustering, pelanggan terbagi ke dalam beberapa segmen utama:

| Segmen | Karakteristik | Rekomendasi |
|---|---|---|
| 💎 Premium | Belanja tinggi, bayar penuh | Tawarkan reward premium |
| 🛍️ Regular Shopper | Belanja rutin, pembayaran normal | Promo cashback regular |
| ⚠️ Cash Advance Heavy | Sering tarik tunai | Edukasi finansial, monitoring |
| 🔴 High Balance | Saldo tinggi, jarang bayar penuh | Penawaran cicilan restrukturisasi |
| 😴 Low Activity | Penggunaan rendah | Reaktivasi dengan insentif |

---