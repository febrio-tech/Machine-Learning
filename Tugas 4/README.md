# Practical Statistics for Data Scientists - O'Reilly

Repository ini berisi kumpulan berkas Jupyter Notebook (`.ipynb`) yang mereproduksi seluruh materi, konsep teori, visualisasi, dan pustaka pemrograman dari buku *Practical Statistics for Data Scientists* (Edisi Kedua) karya Peter Bruce, Andrew Bruce, dan Peter Gedeck. Tujuan utama dari pembuatan notebook ini adalah untuk memfasilitasi pemahaman mendalam terhadap konsep-konsep statistika terapan dalam sains data melalui pendekatan komputasi aktif menggunakan bahasa pemrograman Python. Dengan menerjemahkan teori statistik ke dalam bentuk kode praktis, pembaca diharapkan dapat membangun intuisi analisis data yang kuat secara komputasional.

Link buku : https://drive.google.com/file/d/1dR9228_PRCN5_Hjs9ClxYgKe5zmifkmb/view?usp=sharing

---

## Ringkasan Bab (Chapter Summaries)

Berikut adalah gambaran umum mengenai topik, teori, dan metode yang dibahas pada setiap bab di dalam repository ini:

### 1. [01 - Exploratory Data Analysis.ipynb]
Notebook ini membahas Exploratory Data Analysis (EDA) sebagai tahap awal dalam proyek data science yang bertujuan memahami struktur, pola, dan karakteristik data sebelum pemodelan dilakukan. Pembahasan mencakup klasifikasi jenis data terstruktur (numerik dan kategorikal), konsep data dua dimensi (rectangular data), serta perhitungan ukuran lokasi (mean, median, trimmed mean) dan variabilitas (variance, standard deviation, IQR). Selain itu, dibahas pula teknik eksplorasi distribusi data serta visualisasi hubungan antarvariabel menggunakan scatterplot, hexagonal binning, dan tabel kontingensi.

### 2. [02 - Data and Sampling Distributions.ipynb]
Notebook ini membahas konsep dasar sampling, bias data, dan distribusi sampling yang tetap krusial dalam era data besar (big data). Materi mencakup teknik random sampling dan stratified sampling, identifikasi selection bias, serta fenomena regression to the mean. Lebih lanjut, dibahas pembentukan sampling distribution yang mendasari Central Limit Theorem, teknik resampling menggunakan bootstrap untuk mengestimasi standard error dan confidence interval, serta pengenalan berbagai distribusi probabilitas penting seperti distribusi normal, t, binomial, chi-square, F, Poisson, eksponensial, dan Weibull.

### 3. [03 - Statistical Experiments and Significance Testing.ipynb]
Notebook ini membahas rancangan eksperimen statistik dan uji signifikansi yang digunakan untuk memvalidasi hipotesis dalam proyek data science. Topik utama meliputi konsep A/B testing beserta pentingnya grup kontrol dan randomisasi, formulasi hipotesis nol dan alternatif, serta metode resampling melalui permutation test untuk mendeteksi variasi kebetulan. Selain itu, bab ini menjelaskan pemahaman p-value, uji klasik t-test, ANOVA untuk multi-grup, uji chi-square untuk data kategorikal, risiko multiple testing, pendekatan adaptif multi-arm bandit, serta analisis power dan ukuran sampel.

### 4. [04 - Regression and Prediction.ipynb]
Notebook ini membahas pemodelan regresi linear sederhana dan regresi linear berganda untuk memahami hubungan sebab-akibat antarvariabel sekaligus memprediksi nilai kontinu. Pembahasan meliputi estimasi koefisien menggunakan metode kuadrat terkecil (least squares), interpretasi fitted values dan residual, serta metrik evaluasi model seperti RMSE dan R-squared. Lebih lanjut, bab ini menguraikan teknik seleksi model (stepwise regression), penanganan variabel faktor melalui dummy variables, analisis kolinearitas dan interaksi, diagnostik regresi (outliers, heteroskedastisitas), serta perluasan regresi non-linear seperti regresi polinomial dan spline.

### 5. [05 - Classification.ipynb]
Notebook ini membahas metode klasifikasi sebagai bentuk pembelajaran terbimbing (supervised learning) untuk memprediksi kategori atau kelas dari suatu data. Topik yang dibahas mencakup algoritma Naive Bayes berbasis probabilitas bersyarat, Analisis Diskriminan Linear (LDA) menggunakan matriks kovarians, dan Regresi Logistik untuk estimasi log odds dan probabilitas biner. Bab ini juga menekankan metode evaluasi model klasifikasi menggunakan matriks kebingungan (confusion matrix), metrik akurasi, presisi, recall, kurva ROC, nilai AUC, serta teknik penanganan kelas minoritas yang tidak seimbang (imbalanced data).

### 6. [06 - Statistical Machine Learning.ipynb]
Notebook ini membahas metode pembelajaran mesin berbasis statistik yang menawarkan fleksibilitas lebih tinggi dibandingkan model statistik klasik. Pembahasan diawali dengan algoritma K-Nearest Neighbors (KNN) beserta metrik jarak, standarisasi data, dan penentuan nilai K optimal. Materi dilanjutkan dengan model pohon keputusan (decision trees) berbasis aturan pembagian rekursif serta metrik impuritas Gini dan entropi. Selanjutnya, dibahas konsep ensemble seperti Bagging, Random Forest untuk mengurangi varians, serta Boosting (khususnya XGBoost) untuk meminimalkan bias secara bertahap dengan regularisasi.

### 7. [07 - Unsupervised Learning.ipynb]
Notebook ini membahas metode pembelajaran tidak terbimbing (unsupervised learning) yang bertujuan untuk menemukan struktur internal dan pola tersembunyi pada data tanpa label respons. Pembahasan utama berfokus pada Analisis Komponen Utama (PCA) untuk reduksi dimensi data numerik melalui pembentukan principal components, serta Correspondence Analysis untuk data kategorikal. Selain itu, dijelaskan pula algoritma pengelompokan data seperti K-Means clustering, Hierarchical Clustering yang divisualisasikan melalui dendrogram, serta Model-Based Clustering menggunakan Gaussian Mixture Models dengan evaluasi kriteria BIC.

---

## 🛠️ Teknologi & Kebutuhan Sistem

Proyek ini dibangun menggunakan pustaka Python berikut (disesuaikan dengan kebutuhan analisis pada Notebook 01 - 07):
* **Python** (versi 3.8+)
* **scikit-learn** (pemodelan utama untuk klasifikasi, clustering, PCA, KNN, dan Decision Tree)
* **scipy** & **statsmodels** (perhitungan statistik, uji signifikansi, t-test, ANOVA, dan model regresi)
* **xgboost** (algoritma gradient boosting untuk supervised learning)
* **patsy** (penerjemahan formula statistik untuk analisis regresi)
* **numpy** & **pandas** (pemrosesan data dan komputasi numerik)
* **matplotlib** & **seaborn** (visualisasi data dan grafik statistik)
* **joblib** (serialisasi model)

---

## 🚀 Cara Menjalankan Notebook

1. **Buat virtual environment (opsional tetapi direkomendasikan):**
   ```bash
   python -m venv env
   # Aktifkan di Windows:
   .\env\Scripts\activate
   # Aktifkan di macOS/Linux:
   source env/bin/activate
   ```

2. **Install dependensi yang diperlukan:**
   ```bash
   pip install numpy pandas scikit-learn scipy statsmodels patsy xgboost matplotlib seaborn joblib notebook
   ```

3. **Jalankan Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   Pilih salah satu notebook dari daftar untuk mulai mempelajari materi.

---

## Kesimpulan

Secara keseluruhan, materi yang disajikan dalam repository ini mencakup spektrum dasar statistika deskriptif hingga algoritma machine learning tingkat lanjut untuk sains data. Pembahasan dimulai dari eksplorasi awal struktur data (EDA), pemahaman tentang sampling dan distribusi probabilitas, rancangan eksperimen statistik (A/B testing), serta model regresi dan klasifikasi dasar. Materi kemudian berkembang pada metode tingkat lanjut seperti ensemble machine learning (Random Forest dan Boosting) hingga teknik pembelajaran tidak terbimbing (PCA dan pengelompokan cluster). Melalui reproduksi materi ini, pemahaman yang kuat mengenai landasan statistik yang mendasari analisis data modern dan algoritma machine learning dapat diperoleh secara komprehensif.
