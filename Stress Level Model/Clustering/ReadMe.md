Made by : Istiqomah Auliya Rosyida\
ID : MC211D5X1078\
Path : Machine Learning Untuk Pemula\
Google Colab Link : https://colab.research.google.com/drive/1aev0Mthxa265bku92SaCCNsZ7t0WbIuN?usp=sharing

---

## 📌 Overview

Proyek ini bertujuan untuk mengelompokkan tingkat stres menggunakan algoritma **KMeans Clustering**. Model ini tidak membutuhkan label (unsupervised learning) dan membantu dalam memprediksi tingkat stres pengguna.

---

## 🧠 1. Business Understanding

Tujuan utamanya adalah:
- Mengidentifikasi pola atau kelompok emosi tanpa label eksplisit.
- Menemukan korelasi atau kedekatan antar entri jurnal berdasarkan teksnya.

---

## 📊 2. Data Understanding

### Dataset:
- baris: **108252 baris**
- Kolom: **50 kolom**

### Insight Awal:
- Label terdiri dari: `tidak stres`, `agak stres`, `cukup stres`, `stres`, `stress berat`
- Data digunakan untuk menguji seberapa baik KMeans mengelompokkan teks sesuai pola emosi.

---

## 🧹 3. Data Preparation

Langkah-langkah preprocessing:
* menangani missing value
* mennagani data duplikat
* memilih kolom yang mempengaruhi tingkat stress
* melihat kode unique setiap kolom 
* standarisasi kolom kolom yang ingin di gunakan tadi 
* melihat apakah terdapat oulier 

---

# Membuat file README.md dari template bagian modeling yang telah dirancang

readme_modeling_content = """
## 🤖 4. Modeling

### 📌 Algoritma yang Digunakan:
- **KMeans Clustering**: metode unsupervised learning untuk mengelompokkan data berdasarkan kemiripan fitur.

### 🏗️ Fitur yang Digunakan:
- `Work_stress`
- `Life_satisfaction`
- `Mental_health_state`
- `Age`
- `Worked_job_business`
- `Work_hours`
- `working_status`
- `Mood_disorder`
- `Anxiety_disorder`
- `Gen_health_state`
- `Marital_status`
- `Gender`
- `Total_income`

> Data difiturkan dan diskalakan sebelum modeling.

---

### 🔎 Penentuan Jumlah Cluster

Untuk menentukan jumlah cluster optimal, dilakukan dua metode:

#### 1. **Metode Elbow (Inertia)**
- Plot menunjukkan penurunan inertia paling signifikan pada **k = 2**, sebelum melandai.
- Ini menunjukkan bahwa 2 cluster cukup representatif tanpa overfitting.

#### 2. **Silhouette Score**
Dihitung untuk `k = 2` hingga `k = 10`, hasilnya:

| Jumlah Cluster | Silhouette Score |
|----------------|------------------|
| 2              | **0.3435**       |
| 3              | 0.2412           |
| 4              | 0.2325           |
| 5              | 0.1787           |
| 6              | 0.1762           |
| 7              | 0.1652           |
| 8              | 0.1754           |
| 9              | 0.1786           |
| 10             | 0.1882           |

✅ Hasil terbaik juga pada `k = 2` dengan skor **0.3435**

---

### 📊 Pelatihan Model

Model akhir menggunakan:
python
kmeans = KMeans(n_clusters=2, random_state=42)
kmeans.fit(X_scaled)

---

## 🛠️ Teknologi yang Digunakan

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- PCA untuk visualisasi

---

## 💻 Environment
- **Google Colab** atau Jupyter Notebook
- Python 3.10+

---

## 📂 Output

- Visualisasi distribusi cluster
- Notebook `.ipynb` yang bisa dijalankan ulang

---
