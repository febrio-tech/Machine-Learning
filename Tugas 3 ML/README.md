# Practical Linear Algebra for Data Science - O'Reilly
Repository ini berisi kumpulan berkas Jupyter Notebook (`.ipynb`) yang mereproduksi seluruh materi, konsep teori, visualisasi, dan kode pemrograman dari buku *Practical Linear Algebra for Data Science* karya Mike X Cohen. Tujuan utama dari pembuatan notebook ini adalah untuk memfasilitasi pemahaman mendalam terhadap konsep-konsep aljabar linear melalui pendekatan komputasi aktif menggunakan bahasa pemrograman Python. Dengan mereproduksi teori matematika ke dalam bentuk kode numerik dan visualisasi grafis, pembaca diharapkan dapat membangun intuisi matematika secara lebih konkret dibandingkan dengan hanya mempelajari pembuktian teoretis yang abstrak.

Link buku : https://drive.google.com/file/d/1RPWzRvruRpF59We33k2PGOIexUe-O_dy/view?usp=sharing
---

## Ringkasan Bab (Chapter Summaries)

Berikut adalah gambaran umum mengenai topik, teori, dan algoritma yang dibahas pada setiap bab di dalam repository ini:

### 1. [01 - Introduction.ipynb]
Chapter ini merupakan pengantar yang menjelaskan pentingnya aljabar linear dalam era komputasi modern dan sains data. Fokus pembahasan diarahkan pada perbedaan antara pendekatan aljabar linear tradisional yang abstrak dengan pendekatan aljabar linear modern yang berbasis komputasional. Selain itu, diperkenalkan pula konsep *soft proof* untuk membangun intuisi matematika melalui eksperimen kode Python menggunakan berbagai contoh numerik.

### 2. [02 - Vectors Part 1.ipynb]
Chapter ini membahas konsep dasar vektor sebagai fondasi utama aljabar linear beserta implementasinya menggunakan pustaka NumPy. Pembahasan mencakup representasi geometri dan aljabar, orientasi vektor (baris dan kolom), operasi aritmetika dasar, konsep *dot product*, serta dekomposisi vektor ortogonal. Melalui materi ini, prinsip dasar proyeksi vektor dan pengaruh operasi matematika terhadap dimensi vektor dijelaskan secara terperinci.

### 3. [03 - Vectors Part 2.ipynb]
Chapter ini berfokus pada hubungan timbal balik antara kombinasi linear berbobot (*linear weighted combination*), kebebasan linear (*linear independence*), subruang (*subspace*), rentang (*span*), dan basis. Konsep-konsep tersebut diuraikan untuk memberikan pemahaman mengenai struktur ruang vektor dan dimensi ruang. Pemahaman mendalam pada materi ini menjadi fondasi krusial sebelum mempelajari operasi matriks dan metode reduksi dimensi.

### 4. [04 - Vector Applications.ipynb]
Chapter ini mendemonstrasikan penerapan praktis dari konsep vektor dalam analisis data nyata. Beberapa aplikasi utama yang dibahas meliputi perhitungan koefisien korelasi Pearson, metrik kemiripan kosinus (*cosine similarity*) untuk pemrosesan teks, serta teknik penyaringan deret waktu (*time series filtering*). Selain itu, bab ini juga menguraikan implementasi algoritma pengelompokan *k-means clustering* dari sudut pandang aljabar linear.

### 5. [05 - Matrices, Part 1.ipynb]
Chapter ini memperkenalkan matriks sebagai objek matematika dua dimensi yang bertindak sebagai perluasan dari vektor. Pembahasan diawali dengan pembuatan dan visualisasi matriks, pengenalan matriks khusus seperti matriks identitas dan diagonal, serta operasi elemen-demi-elemen (*element-wise*). Selanjutnya, dibahas pula operasi perkalian matriks standar, perkalian matriks-vektor, sifat transposisi termasuk aturan *LIVE EVIL*, serta karakteristik matriks simetris.

### 6. [06 - Matrices, Part 2.ipynb]
Chapter ini membahas konsep-konsep tingkat lanjut pada matriks yang penting dalam aljabar linear terapan. Topik utama mencakup perhitungan norma matriks (*matrix norms*), identifikasi ruang matriks (*matrix spaces*), serta penentuan peringkat matriks (*rank*). Lebih lanjut, diuraikan pula konsep determinan dan persamaan polinomial karakteristik yang menjadi dasar dari analisis transformasi linear.

### 7. [07 - Matrix Applications.ipynb]
Chapter ini mengulas berbagai aplikasi matriks dalam pemrosesan data dan citra digital. Pembahasan meliputi pembentukan matriks kovarians dan korelasi untuk analisis multivariat, serta penerapan matriks transformasi untuk translasi, rotasi, dan penskalaan geometri data spasial. Bab ini juga membahas penggunaan kernel matriks dalam operasi konvolusi untuk deteksi fitur atau tepi pada citra.

### 8. [08 - Matrix Inverse.ipynb]
Chapter ini menjelaskan konsep invers matriks persegi ($A^{-1}$) sebagai salah satu pilar penyelesaian persamaan sistem linear $Ax = b$. Pembahasan mencakup syarat keterbalikan matriks (kondisi *invertibility*), hubungan antara invers dengan determinan, serta metode komputasi invers matriks. Selain itu, dibahas pula limitasi numerik dan ketidakstabilan komputasional yang dapat terjadi saat menghitung invers matriks dalam aplikasi praktis.

### 9. [09 - Orthogonal Matrices and QR Decomposition.ipynb]
Chapter ini membahas karakteristik matriks ortogonal yang memiliki sifat unik berupa nilai transpos yang sama dengan inversnya ($Q^T = Q^{-1}$). Pembahasan mencakup prosedur ortogonalisasi Gram-Schmidt untuk mengubah basis vektor sembarang menjadi basis ortonormal. Lebih lanjut, diuraikan algoritma dekomposisi QR ($A = QR$) beserta aplikasinya untuk meningkatkan stabilitas numerik dalam perhitungan invers matriks.

### 10. [10 - Row Reduction and LU Decomposition.ipynb]
Chapter ini menyajikan metode penyelesaian sistem persamaan linear secara sistematis melalui operasi baris elementer (*row reduction*). Topik pembahasan meliputi algoritma eliminasi Gaussian dan Gauss-Jordan untuk menghasilkan bentuk eselon baris terreduksi (RREF). Bab ini juga memperkenalkan dekomposisi LU ($A = LU$) yang memfaktorkan matriks menjadi matriks segitiga bawah (*lower*) dan segitiga atas (*upper*) guna efisiensi komputasi.

### 11. [11 - General Linear Models and Least Squares.ipynb]
Chapter ini mengulas formulasi Model Linear Umum (*General Linear Model* / GLM) dan metode kuadrat terkecil (*least squares*) sebagai fondasi statistika dalam aljabar linear terapan. Pembahasan mencakup penyusunan matriks desain (*design matrix*), proyeksi orthogonal data ke dalam subruang model, serta penurunan persamaan normal untuk mengestimasi parameter model. Pendekatan ini memperlihatkan bagaimana hubungan sebab-akibat antar variabel data dapat dimodelkan secara matematis.

### 12. [12 - Least Squares Applications.ipynb]
Chapter ini mendemonstrasikan aplikasi metode *least squares* pada data riil serta teknik-teknik optimasi model dalam statistika dan *machine learning*. Topik yang dibahas meliputi penanganan masalah multikolinearitas melalui metode regularisasi L1 (Lasso) dan L2 (Ridge). Di samping itu, diuraikan pula implementasi regresi polinomial untuk memodelkan hubungan non-linear serta metode pencarian parameter optimal (*grid search*).

### 13. [13 - Eigendecomposition.ipynb]
Chapter ini membahas konsep dekomposisi spektral atau *eigendecomposition* pada matriks persegi. Fokus utama diarahkan pada pencarian pasangan nilai eigen (*eigenvalues*) dan vektor eigen (*eigenvectors*) yang merepresentasikan arah transformasi invarian dari suatu matriks. Selain itu, bab ini juga membahas teorema spektral untuk matriks simetris serta sifat-sifat aljabar dan geometri dari nilai eigen.

### 14. [14 - Singular Value Decomposition.ipynb]
Chapter ini menguraikan dekomposisi nilai singular (*Singular Value Decomposition* / SVD) sebagai salah satu metode faktorisasi matriks paling serbaguna. Berbeda dengan *eigendecomposition*, SVD dapat diterapkan pada semua jenis matriks, baik persegi maupun non-persegi. Pembahasan mencakup struktur matriks ortogonal kiri ($U$), matriks diagonal nilai singular ($\Sigma$), dan matriks ortogonal kanan ($V$), serta hubungan matematis antara SVD dengan *eigendecomposition*.

### 15. [15 - Eigendecomposition and SVD Applications.ipynb]
Chapter ini membahas berbagai aplikasi penting dari *eigendecomposition* dan SVD dalam memecahkan masalah sains data nyata. Fokus bahasan meliputi algoritma *Principal Component Analysis* (PCA) untuk reduksi dimensi tanpa kehilangan informasi penting, aproksimasi rank rendah (*low-rank approximation*) untuk kompresi data, dan teknik rekonstruksi citra untuk pembersihan derau (*image denoising*). Melalui bab ini, dipaparkan bagaimana teori dekomposisi diwujudkan menjadi solusi komputasional yang efisien.

---

## 🛠️ Teknologi & Kebutuhan Sistem

Proyek ini dibangun menggunakan pustaka Python berikut:
* **Python** (versi 3.8+)
* **numpy** (komputasi numerik dan operasi matriks/vektor)
* **scipy** (aljabar linear tingkat lanjut seperti dekomposisi LU)
* **scikit-learn** (pemodelan utama untuk PCA dan LDA)
* **matplotlib** (visualisasi data dan representasi geometri)

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
   pip install numpy scipy scikit-learn matplotlib notebook
   ```

3. **Jalankan Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   Pilih salah satu notebook dari daftar untuk mulai mempelajari materi.

---

## Kesimpulan

Secara keseluruhan, materi yang disajikan dalam repository ini mencakup spektrum dasar hingga tingkat lanjut aljabar linear terapan untuk sains data. Pembahasan dimulai dari elemen paling sederhana berupa vektor dan matriks beserta operasi dasarnya, dilanjutkan dengan konsep sistem persamaan linear dan metode transformasi geometri. Materi kemudian berkembang pada metode dekomposisi matriks utama seperti QR, LU, *eigendecomposition*, dan *Singular Value Decomposition* (SVD), hingga penerapannya dalam penyelesaian masalah regresi *least squares* serta analisis multivariat sains data (seperti PCA). Melalui penguasaan materi di dalam repository ini, pemahaman komprehensif mengenai bagaimana aljabar linear mendasari berbagai algoritma komputasi modern dan sains data dapat diperoleh secara utuh.

