# Portofolio: Deteksi Penipuan (Fraud) & Segmentasi Nasabah Bank

Proyek ini adalah *submission* untuk kelas **Belajar Machine Learning untuk Pemula** di Dicoding. Proyek ini mendemonstrasikan alur kerja *End-to-End Machine Learning*, mulai dari pembersihan data, *clustering* (*unsupervised*), hingga klasifikasi (*supervised*) untuk mengidentifikasi pola transaksi.

## 🎯 Tujuan Proyek

Tujuan dari proyek ini adalah:
1.  **Clustering (Unsupervised):** Mengelompokkan nasabah ke dalam beberapa cluster berdasarkan perilaku transaksi mereka menggunakan algoritma K-Means.
2.  **Klasifikasi (Supervised):** Membangun model klasifikasi yang dapat memprediksi *cluster* (target) seorang nasabah berdasarkan data transaksinya.

---

## 🚀 Alur Pengerjaan

Proyek ini dibagi menjadi dua *notebook* utama:

### 1. Notebook Clustering
* **Pembersihan Data:** Menangani nilai null dan duplikat.
* **Pra-pemrosesan:**
    * **StandardScaler:** Melakukan standarisasi pada fitur numerik.
    * **LabelEncoder:** Mengubah fitur kategorikal menjadi numerik.
    * **Handling Outlier:** Menggunakan metode IQR untuk membersihkan data.
* **Reduksi Dimensi:** Menggunakan **PCA (Principal Component Analysis)** untuk visualisasi data.
* **Pemodelan (K-Means):**
    * Menggunakan **Elbow Method** dan **Silhouette Score** untuk menentukan jumlah cluster optimal (K=4).
    * Melatih model **K-Means Clustering** untuk mengelompokkan data.
    * Menyimpan data yang sudah memiliki label cluster ke `data_clustering.csv`.

### 2. Notebook Klasifikasi
* **Pra-pemrosesan:** Menggunakan **One-Hot Encoding** (`pd.get_dummies`) pada data kategorikal.
* **Persiapan Data:** Melakukan **Train-Test Split** (80% latih, 20% uji).
* **Pemodelan (Mandatory):**
    * Melatih model **Decision Tree Classifier**.
    * Hasil: **Akurasi 98%**
* **Pemodelan (Eksplorasi):**
    * Melatih model **Random Forest Classifier**.
    * Hasil: **Akurasi 99%**
* **Optimasi Model:**
    * Melakukan **Hyperparameter Tuning** pada Random Forest menggunakan **GridSearchCV**.
    * **Hasil Akhir (Model Terbaik): Akurasi 99%**

---

## 🛠️ Teknologi yang Digunakan

* Python 3
* Pandas & Numpy
* Scikit-learn (PCA, K-Means, DecisionTree, RandomForest, GridSearchCV)
* Joblib (untuk menyimpan model)
* Matplotlib & Seaborn (untuk visualisasi)

---

## 🏁 Cara Menjalankan Proyek

1.  **Clone Repositori**
    ```bash
    git clone [https://github.com/abdullatiefmufti/Deteksi-Penipuan-Fraud-Detection-dan-Identifikasi-Transaksi-Bank.git](https://github.com/abdullatiefmufti/Deteksi-Penipuan-Fraud-Detection-dan-Identifikasi-Transaksi-Bank.git)
    ```

2.  **Masuk ke Direktori**
    ```bash
    cd Deteksi-Penipuan-Fraud-Detection-dan-Identifikasi-Transaksi-Bank
    ```

3.  **(Opsional) Buat Virtual Environment**
    ```bash
    python -m venv venv
    source venv/bin/activate  # (Di Windows: venv\Scripts\activate)
    ```

4.  **Install Dependencies**
    *(Pastikan Anda membuat file `requirements.txt` terlebih dahulu)*
    ```bash
    pip install -r requirements.txt
    ```

5.  **Jalankan Notebook**
    Buka folder `notebooks/` dan jalankan file `.ipynb` menggunakan Jupyter Notebook atau Google Colab.

---

## 📂 Struktur Repositori

Deteksi-Penipuan-Fraud-Detection-dan-Identifikasi-Transaksi-Bank/ ├── notebooks/ │ ├── [Clustering]_Submission_Akhir_BMLP_ltp_dull.ipynb │ └── [Klasifikasi]_Submission_Akhir_BMLP_ltp_dull.ipynb ├── data/ │ ├── data_clustering.csv │ └── data_clustering_inverse.csv ├── models/ │ ├── model_clustering.h5 │ ├── PCA_model_clustering.h5 │ ├── decision_tree_model.h5 │ ├── explore_RandomForestClassifier_classification.h5 │ └── tuning_classification.h5 ├── README.md └── requirements.txt
