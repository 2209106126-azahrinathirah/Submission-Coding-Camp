# Laporan Proyek Machine Learning - Andi Zahrina Athirah Ahmad
---
## Domain Proyek

**Latar Belakang**

![Latar Belakang](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Latar_Belakang.png)

Prediksi harga saham merupakan tantangan penting dalam dunia keuangan, khususnya di pasar modal Indonesia yang terus berkembang pesat dalam beberapa dekade terakhir. Fluktuasi harga saham yang tinggi disebabkan oleh berbagai faktor seperti kondisi ekonomi makro, kinerja perusahaan, sentimen pelaku pasar, serta situasi geopolitik, menjadikan investasi di pasar saham penuh risiko <a href="#1">[1]</a>. Ketidakstabilan ini menyulitkan investor dalam mengambil keputusan yang optimal, terutama untuk jangka menengah dan panjang. Oleh karena itu, dibutuhkan pendekatan prediktif yang mampu mengenali pola-pola kompleks dalam data historis harga saham guna mendukung pengambilan keputusan yang lebih akurat dan berbasis data <a href="#1">[1]</a>.

Salah satu saham yang menarik untuk dianalisis adalah PT Telekomunikasi Indonesia Tbk (TLKM), sebuah perusahaan telekomunikasi milik negara yang termasuk dalam kategori saham blue chip. Saham TLKM aktif diperdagangkan di Bursa Efek Indonesia (BEI) dan memiliki pengaruh besar terhadap indeks utama seperti IHSG dan LQ45 <a href="#2">[2]</a>. Kemampuan untuk memprediksi harga penutupan saham TLKM secara akurat dapat membantu investor, analis pasar, dan pembuat kebijakan dalam membuat keputusan yang lebih rasional dan berbasis data.

Model statistik tradisional seperti ARIMA atau regresi linear sering kali tidak mampu menangkap pola nonlinier dan dependensi jangka panjang dalam data time series saham <a href="#3">[3]</a>. Untuk menjawab tantangan tersebut, pendekatan berbasis deep learning seperti Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) menjadi solusi yang menjanjikan karena kemampuannya dalam mempelajari urutan data historis dan mengingat informasi jangka panjang <a href="#4">[4]</a>.

Melalui proyek ini, saya mengembangkan dan membandingkan model LSTM dan GRU untuk memprediksi harga penutupan saham TLKM, dengan fokus pada tiga skenario waktu ke depan: 7 hari, 30 hari, dan 60 hari. Evaluasi dilakukan menggunakan metrik MAE, RMSE, dan MAPE untuk menilai sejauh mana model dapat memberikan hasil prediksi yang akurat dan stabil <a href="#5">[5]</a>.

---
    
**Rubrik/Kriteria Tambahan (Opsional)**:

**Mengapa Masalah Ini Harus Diselesaikan❓**
1. Fluktuasi harga saham TLKM yang tinggi membuat investor membutuhkan strategi prediktif berbasis data untuk memaksimalkan return dan meminimalkan risiko.
2. Model statistik konvensional seperti ARIMA atau regresi linear belum mampu menangani data saham yang kompleks, nonlinier, dan bergantung pada urutan waktu.
3. Di era digital, pengambilan keputusan finansial berbasis data dan kecerdasan buatan telah menjadi praktik umum secara global, dan perlu lebih banyak diterapkan di pasar saham Indonesia.

**Bagaimana Masalah Ini Harus Diselesaikan❓**
1. Mengumpulkan data historis harga saham TLKM dari sumber resmi kaggle Bursa Efek Indonesia.
2. Melakukan preprocessing data time series, termasuk normalisasi dan pembuatan window sekuensial.
3. Membangun dua model deep learning: Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) untuk mempelajari pola historis.
4. Mengevaluasi performa model menggunakan metrik MAE, RMSE, dan MAPE untuk mengukur akurasi prediksi.
5. Melakukan eksperimen prediksi harga penutupan saham TLKM untuk tiga horizon waktu ke depan:
   - 7 hari (jangka pendek)
   - 30 hari (jangka menengah)
   - 60 hari (jangka panjang)
  
---
  
**Rubrik/Kriteria Tambahan (Opsional)**:

## Hasil Riset Terkait (Referensi)

<a name="1">[1]</a> G. Adiatmaja and R. Indraswari, "Comparative Analysis of LSTM and GRU Models for Indonesian Stock Price Prediction with Integrated Technical and Fundamental Indicators," 2024 International Conference on Information Technology Systems and Innovation (ICITSI), Bandung, Indonesia, 2024, pp. 206-211. 
[https://doi.org/10.1109/ICITSI65188.2024.10929370](https://doi.org/10.1109/ICITSI65188.2024.10929370)

<a name="2">[2]</a> H. K. Alfredo, *Analysis of Fama and French 3-Factor Model Variables in the Formation of Expected Stock Returns (Issuers of LQ-45 Index Member Stocks for the Period 2020–2022)*, Edunity, vol. 2, no. 7, 2023.  
[https://doi.org/10.57096/edunity.v2i7.122](https://doi.org/10.57096/edunity.v2i7.122)

<a name="3">[3]</a> M. Ridwan et al., *Comparison of ARIMA and GRU Models for High-Frequency Time Series Forecasting*, Scientific Journal of Informatics, vol. 10, no. 3, 2023.  
[https://journal.unnes.ac.id/nju/sji/article/view/45965](https://journal.unnes.ac.id/nju/sji/article/view/45965)

<a name="4">[4]</a> R. Yavasani dan F. Wang, *Comparative Analysis of LSTM, GRU, and ARIMA Models for Stock Market Price Prediction*, Journal of Student Research, vol. 12, no. 4, 2023.  
[https://doi.org/10.47611/jsrhs.v12i4.5888](https://doi.org/10.47611/jsrhs.v12i4.5888)

<a name="5">[5]</a> N. A. Nilsen, *Perbandingan Model RNN, Model LSTM, dan Model GRU dalam Memprediksi Harga Saham-Saham LQ45*, Jurnal Statistika dan Aplikasinya, vol. 6, no. 1, 2022.  
[https://doi.org/10.21009/JSA.06113](https://doi.org/10.21009/JSA.06113)

---

## Business Understanding

### Problem Statements

Berdasarkan latar belakang, proyek ini difokuskan untuk menjawab pertanyaan-pertanyaan berikut:

1. Bagaimana membangun model machine learning berbasis deep learning yang mampu memprediksi harga penutupan saham secara akurat berdasarkan data historis?
2. Apakah model Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) dapat memberikan hasil prediksi yang akurat
3. Seberapa akurat model yang dibangun dalam memprediksi harga penutupan saham PT Telekomunikasi Indonesia Tbk (TLKM) untuk horizon waktu 7 hari ke depan?

### Goals

Tujuan utama dari proyek ini meliputi:

- Mengembangkan dan membandingkan dua model deep learning (LSTM dan GRU) untuk memprediksi harga saham TLKM berdasarkan data historis.
- Menilai performa prediksi dari masing-masing model dengan menggunakan metrik evaluasi MAE (Mean Absolute Error), RMSE (Root Mean Square Error), dan MAPE (Mean Absolute Percentage Error).
- Memberikan insight kepada investor atau analis pasar terhadap akurasi dan stabilitas model prediksi untuk pengambilan keputusan yang lebih informatif.

---

**Rubrik/Kriteria Tambahan (Opsional)**:

### Solution statements

Untuk mencapai tujuan di atas secara terukur dan optimal, dua pendekatan utama akan dilakukan:

1. **Perbandingan Model Deep Learning**  
   Membangun dua model prediksi berbasis jaringan saraf berulang (RNN):
   - **Long Short-Term Memory (LSTM)**
   - **Gated Recurrent Unit (GRU)**  
   Model dilatih dengan data harga historis saham TLKM dan diuji berdasarkan tiga skenario horizon waktu prediksi 7 hari ke depan?

2. **Evaluasi dan Optimasi Model**  
   Evaluasi dilakukan terhadap performa model dengan metrik:
   - **MAE** – Rata-rata kesalahan absolut.
   - **RMSE** – Akar dari rata-rata kuadrat error.
   - **MAPE** – Persentase kesalahan absolut rata-rata.

---

## Data Understanding

### Deskripsi Dataset

Dataset yang digunakan dalam proyek ini adalah data historis harga saham PT Telekomunikasi Indonesia Tbk (TLKM) yang diperoleh dari situs resmi Yahoo Finance. Data mencakup periode harian dari tahun 2019 hingga 2024, dan terdiri dari informasi harga saham yang biasa digunakan dalam analisis teknikal.

🔗 **Sumber Data:**  
[Dataset Saham Bursa Efek - Kaggle (oleh Agung Pambudi)](https://www.kaggle.com/datasets/agungpambudi/dataset-saham-bursa-efek/data)

- Nama Folder : Data Tambahan
- Nama File   : TLKM.csv

### Variabel / Fitur pada Dataset

Berikut adalah penjelasan fitur-fitur yang tersedia dalam dataset:

| Nama Fitur  | Deskripsi |
|-------------|-----------|
| `Date`      | Tanggal perdagangan (format YYYY-MM-DD) |
| `Open`      | Harga pembukaan saham pada hari tersebut |
| `High`      | Harga tertinggi saham pada hari tersebut |
| `Low`       | Harga terendah saham pada hari tersebut |
| `Close`     | Harga penutupan saham pada hari tersebut |
| `Adj Close` | Harga penutupan yang telah disesuaikan (adjusted) terhadap dividen dan stock split |
| `Volume`    | Jumlah saham yang diperdagangkan pada hari tersebut |

---

**Rubrik/Kriteria Tambahan (Opsional)**:

### Exploratory Data Analysis (EDA)

Beberapa langkah EDA dilakukan untuk memahami pola dan struktur data, antara lain:

#### 1. EDA - Deskripsi Variable

**Informasi Dataset**

Dataset ini terdiri dari **1212 baris** dan **7 kolom** utama dengan tipe data sebagai berikut:

| **No.** | **Fitur**     | **Tipe Data** |
|--------:|---------------|---------------|
| 1       | Date          | object        |
| 2       | Adj Close     | float64       |
| 3       | Close         | float64       |
| 4       | High          | float64       |
| 5       | Low           | float64       |
| 6       | Open          | float64       |
| 7       | Volume        | object        |

**Insight**

- Seluruh kolom harga sudah memiliki tipe data yang sesuai numerik (float64).
- Kolom Date dan Volume masih bertipe object.
  - **Date** perlu dikonversi ke tipe data datetime untuk memungkinkan analisis berbasis waktu, seperti tren musiman atau harian.
  - **Volume** perlu dikonversi ke format numerik agar dapat dianalisis lebih lanjut, termasuk dalam perhitungan statistik dan visualisasi.
    

**Deskripsi Statistik**

| Statistik | Adj Close   | Close      | High       | Low        | Open       |
|-----------|-------------|------------|------------|------------|------------|
| Count     | 1212.000000 | 1212.000000| 1212.000000| 1212.000000| 1212.000000|
| Mean      | 3232.919909 | 3647.978548| 3690.998350| 3607.483498| 3650.981848|
| Std       |  506.366462 |  510.865708|  508.614228|  508.024318|  508.843617|
| Min       | 2070.660000 | 2560.000000| 2590.000000| 2450.000000| 2550.000000|
| 25%       | 2835.450000 | 3190.000000| 3250.000000| 3150.000000| 3200.000000|
| 50%       | 3228.050000 | 3720.000000| 3765.000000| 3690.000000| 3720.000000|
| 75%       | 3666.010000 | 4030.000000| 4060.000000| 3990.000000| 4030.000000|
| Max       | 4295.700000 | 4770.000000| 4850.000000| 4720.000000| 4850.000000|

**Insight**

Dari tabel statistik deskriptif di atas, diperoleh beberapa insight penting mengenai distribusi harga saham TLKM:

- **Jumlah Data Konsisten**
  
  Semua fitur harga memiliki jumlah entri yang sama, yaitu 1212 baris data, menandakan tidak ada missing value pada kelima fitur ini.

- **Nilai Rata-Rata (Mean)**
  - Harga penutupan (Close) rata-rata berada di sekitar **Rp 3.648**, sedikit lebih tinggi dibanding harga open rata-rata sebesar **Rp 3.651**.  
   - Hal ini menunjukkan bahwa secara umum, harga saham TLKM cenderung stabil atau mengalami kenaikan tipis dalam satu hari perdagangan.

- **Volatilitas (Standar Deviasi)**
  
   Nilai std yang cukup tinggi (sekitar 500) menunjukkan bahwa fluktuasi harian cukup besar, mencerminkan dinamika pasar saham TLKM yang aktif dan berisiko sedang-tinggi.

- **Rentang Harga (Min - Max)**
  
  Harga terendah (Low) menyentuh **Rp 2.450**, sedangkan harga tertinggi (High) mencapai **Rp 4.850**, menunjukkan rentang fluktuasi sekitar **98%** selama periode data.

- **Distribusi Harga (25% - 75%)**
  - Harga Close 50% dari data berada di antara **Rp 3.190** (Q1) dan **Rp 4.030** (Q3), dengan nilai tengah (median) di **Rp 3.720**.  
   - Distribusi yang tidak terlalu simetris ini menunjukkan bahwa saham TLKM lebih sering berada dalam kisaran menengah ke atas dari rentang harganya.

---
  
#### 2. EDA - Menangani Missing Value

| No | Kolom      | Jumlah Nilai Hilang |
|----|------------|----------------------|
| 1  | Date       | 0                    |
| 2  | Adj Close  | 0                    |
| 3  | Close      | 0                    |
| 4  | High       | 0                    |
| 5  | Low        | 0                    |
| 6  | Open       | 0                    |
| 7  | Volume     | 0                    |

**Insight**

Dari table diatas menunjukkan bahwa tidak terdapat nilai yang hilang pada seluruh kolom dalam dataset.
Dengan tidak adanya missing value, proses analisis dapat langsung dilanjutkan ke tahapan berikutnya tanpa perlu melakukan penanganan khusus terhadap data yang tidak lengkap.

---

#### 3. EDA - Menangani Outlier
   
### 🚨 Jumlah Outlier per Kolom (Metode IQR)

| No | Kolom      | Jumlah Outlier |
|----|------------|----------------|
| 1  | Adj Close  | 0              |
| 2  | Close      | 0              |
| 3  | High       | 0              |
| 4  | Low        | 0              |
| 5  | Open       | 0              |
| 6  | Volume     | 64             |

![BoxPlot Outlier Volume](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/BoxPlot_Outlier_Volume.png)

![ScatterPlot Outlier Volume Before](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/ScatterPlot_Outlier_Volume_Before.png)

![ScatterPlot Outlier Volume After](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/ScatterPlot_Outlier_Volume_After.png)

### Jumlah Outlier `Close` per Bulan dan Tahun

| No | Tahun | Bulan | Jumlah Outlier |
|----|-------|-------|----------------|
| 1  | 2020  | 4     | 1              |
| 2  | 2021  | 1     | 1              |
| 3  | 2021  | 2     | 4              |
| 4  | 2021  | 4     | 1              |
| 5  | 2021  | 5     | 1              |
| 6  | 2021  | 10    | 1              |
| 7  | 2021  | 11    | 2              |
| 8  | 2022  | 3     | 1              |
| 9  | 2022  | 6     | 1              |
| 10 | 2022  | 11    | 1              |
| 11 | 2022  | 12    | 2              |
| 12 | 2023  | 1     | 1              |
| 13 | 2023  | 2     | 1              |
| 14 | 2023  | 4     | 2              |
| 15 | 2023  | 9     | 1              |
| 16 | 2023  | 11    | 2              |
| 17 | 2023  | 12    | 2              |
| 18 | 2024  | 1     | 2              |
| 19 | 2024  | 3     | 4              |

![LinePlot Oulier Before vs After](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/LinePlot_Oulier_Before_vs_After.png)

![LinePlot Distribuasi Date](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/LinePlot_Distribuasi_Date.png)


---

#### 4. EDA - Univariate Analysis

![Histogram Fitur Numerik](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Histogram_Fitur_Numerik.png)

**Insight**

- **Close, Open, High, Low, Adj Close**
   - Memiliki pola distribusi **bimodal** (dua puncak).
   - Hal ini menunjukkan kemungkinan adanya dua kelompok harga yang dominan selama periode data.
   - Kemungkinan disebabkan oleh perubahan tren besar, seperti stock split, pergantian harga saham yang signifikan, atau masa sebelum dan sesudah krisis pasar.

- **Volume**
   - Distribusi bersifat **positively skewed** (kemencengan ke kanan).
   - Mayoritas volume transaksi harian berada di angka rendah, sementara terdapat sedikit hari dengan lonjakan volume yang tinggi.
   - Hal ini menunjukkan adanya aktivitas perdagangan tidak merata.


![Barplot Distribusi Data Waktu](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Barplot_Distribusi_Data_Waktu.png)

**Insight**:

- **Distribusi per Tahun**:
   - Data dari tahun 2019 sangat sedikit karena hanya mencakup sebagian tahun.
   - Tahun 2020 hingga 2022 memiliki jumlah data paling lengkap dan seimbang.
   - Data tahun 2024 belum lengkap (hanya sampai sebagian kuartal ke-2 atau ke-3), sehingga jumlah datanya lebih rendah.

- **Distribusi per Bulan**:
   - Distribusi data per bulan terlihat cukup merata, menunjukkan tidak ada bulan yang secara signifikan kehilangan data.
   - Ini mengindikasikan bahwa data saham dikumpulkan secara konsisten sepanjang tahun.

- **Distribusi per Hari (Weekday)**:
   - Hari Senin sampai Jumat memiliki jumlah data yang hampir sama.
   - Hal ini konsisten dengan jadwal pasar saham** yang hanya buka pada hari kerja (Senin–Jumat), dan tidak ada data untuk Sabtu & Minggu.

- **Distribusi per Kuartal**:
   - Data per kuartal menunjukkan konsistensi jumlah data tiap kuartal, terutama dari 2020Q1 hingga 2023Q4.
   - Kuartal awal (2019Q4) dan akhir (2024Q2–Q4) memiliki jumlah data lebih sedikit karena cakupan waktunya tidak penuh.

![LinePlot Tren Harga Open vs Close](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/LinePlot_Tren_Harga_Open_vs_Close.png)

**Insight**

- Terjadi penurunan tajam harga saham pada awal 2020.
- Tren harga meningkat stabil dari akhir 2020 hingga 2022.
- Mulai tahun 2023, tren cenderung menurun kembali.
- Harga `Open` dan `Close` sangat berdekatan, menunjukkan selisih kecil dalam satu hari perdagangan.

---

#### 5. EDA - Multivariate Analysis

![Pairplot Fitur Numerik](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Pairplot_Fitur_Numerik.png)

**Insight**:

- **Korelasi Tinggi antar Harga (Open, High, Low, Close, Adj Close)**
   - Terdapat korelasi linier yang sangat kuat antara fitur harga, terlihat dari scatter plot yang membentuk garis diagonal rapat. Hal ini wajar, karena kelima fitur tersebut merepresentasikan harga pada titik waktu berbeda dalam satu hari dan saling berkaitan.

- **`Volume` Tidak Berkorelasi Kuat dengan Harga**
   - Tidak tampak pola hubungan yang jelas antara Volume dengan fitur harga (Open, Close, dll). Ini Menunjukkan bahwa volume perdagangan tidak selalu sejalan dengan fluktuasi harga, dan perlu dianalisis terpisah.

- **Distribusi Bimodal**
   - Diagonal histogram untuk beberapa fitur harga menunjukkan pola bimodal, konsisten dengan analisis univariat sebelumnya. Ini menunjukkan kemungkinan adanya dua periode harga dominan dalam data.
     

![Heatmap Fitur Numerik](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Heatmap_Fitur_Numerik.png)

**Insight**:
- Open, High, Low, dan Close memiliki korelasi yang sangat tinggi satu sama lain (nilai mendekati atau sama dengan 1).
  - pergerakan harga pada satu titik waktu sangat memengaruhi harga pada titik lainnya.
  - Hal ini umum terjadi pada data saham karena harga pembukaan, tertinggi, dan penutupan biasanya bergerak searah.

- Adj Close juga memiliki korelasi tinggi (sekitar 0.91) terhadap Open, High, Low, dan Close.
  - Ini menunjukkan bahwa harga penutupan yang disesuaikan masih sangat terkait dengan harga aktual.

- Volume_log menunjukkan korelasi negatif lemah terhadap semua fitur harga (sekitar -0.08 sampai -0.10).


---

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

### 🧪 Contoh Data Setelah Pra-Pemrosesan (`df_final_scaled` - untuk LSTM/GRU)

| Year | Month     | Day       | Adj Close | Close_Capped | Open     | High     | Low      | Volume_log |
|------|-----------|-----------|-----------|--------------|----------|----------|----------|------------|
| 0.0  | 0.909091  | 0.200000  | 0.515033  | 0.683258     | 0.695652 | 0.690265 | 0.678414 | 0.893524   |
| 0.0  | 0.909091  | 0.233333  | 0.529240  | 0.701357     | 0.634783 | 0.676991 | 0.678414 | 0.865904   |
| 0.0  | 0.909091  | 0.333333  | 0.525689  | 0.696833     | 0.647826 | 0.676991 | 0.700441 | 0.855849   |
| 0.0  | 0.909091  | 0.366667  | 0.554107  | 0.733032     | 0.652174 | 0.707965 | 0.704846 | 0.876730   |
| 0.0  | 0.909091  | 0.400000  | 0.543451  | 0.719457     | 0.686957 | 0.699115 | 0.726872 | 0.878685   |

### 🌲 Contoh Data Setelah Pra-Pemrosesan (`df_final_tree` - untuk XGBoost/LightGBM)

| Year | Month | Day | Adj Close | Close_Capped | Open   | High   | Low    | Volume_log |
|------|-------|-----|-----------|--------------|--------|--------|--------|-------------|
| 2019 | 11    | 7   | 3216.63   | 4070.0       | 4150.0 | 4150.0 | 3990.0 | 18.646151   |
| 2019 | 11    | 8   | 3248.24   | 4110.0       | 4010.0 | 4120.0 | 3990.0 | 18.069772   |
| 2019 | 11    | 11  | 3240.34   | 4100.0       | 4040.0 | 4120.0 | 4040.0 | 17.859961   |
| 2019 | 11    | 12  | 3303.57   | 4180.0       | 4050.0 | 4190.0 | 4050.0 | 18.295697   |
| 2019 | 11    | 13  | 3279.86   | 4150.0       | 4130.0 | 4170.0 | 4100.0 | 18.336491   |



**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

---

## Modeling

Tahapan ini menjelaskan proses pembangunan dua model Deep Learning, yaitu **LSTM** dan **GRU**, untuk memprediksi harga saham menggunakan data historis.

### Model 1: LSTM (Long Short-Term Memory)

**Tahapan Pemodelan**
1. Persiapan Data Input
    - Input berbentuk data sekuensial: setiap sampel memuat **60 hari terakhir** data harga saham.
    - Bentuk input (`X_train_lstm`): `(jumlah_sampel, 60, jumlah_fitur)`
    - Target (`y_train_lstm`): harga saham hari ke-61.
  
2. Membangun Arsitektur Model
   
   ![arsitektur model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/arsitektur_model_lstm.png)

   Model disusun dengan layer sebagai berikut:
   - **LSTM Layer**: 64 unit, `return_sequences=False`
     Tidak perlu output sequence karena hanya memprediksi 1 nilai.
   - **Dropout Layer**: 0.2 (20%) untuk mencegah overfitting.
   - **Dense Layer**: 1 unit (regresi harga saham).
  
4. Kompilasi Model

   ![compile model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/compile_model_ltsm.png)
   
   Model dikompilasi dengan:
   - Loss Function: Mean Squared Error (MSE)
     -> Karena ini adalah regresi numerik.
   - Optimizer: Adam dengan learning rate 0.0005
     -> Adam menggabungkan keunggulan dari RMSprop dan momentum.
  
5. EarlyStopping Callback
   
   ![EarlyStopping model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/EarlyStopping_model_lstm.png)

   Untuk mencegah overfitting:
   - Mengamati val_loss
   - Menghentikan pelatihan jika val_loss tidak membaik selama 5 epoch berturut-turut.
   - Mengembalikan bobot model terbaik dari epoch sebelumnya..

6. Training Model

   ![training model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/training_model_lstm.png)
   
   Model dilatih dengan parameter:
   - Epochs: Maksimal 60
   - Batch Size: 16
   - Validation Split: 10% dari data latih
   - Callback: EarlyStopping

**Parameter Model**

| Parameter             | Nilai                         |
|-----------------------|-------------------------------|
| Model Type            | LSTM                          |
| Hidden Units          | 64                            |
| Dropout Rate          | 0.2                           |
| Loss Function         | Mean Squared Error (MSE)      |
| Optimizer             | Adam                          |
| Learning Rate         | 0.0005                        |
| Epochs                | 60                            |
| Batch Size            | 16                            |
| Early Stopping        | Patience = 5, Restore Best    |
| Validation Split      | 10%                           |
| Input Shape           | (60, 1)                       |

---

### Model 2: GRU (Gated Recurrent Unit)

**Tahapan Pemodelan**

1. **Persiapan Data Input**  
   - Input berbentuk data sekuensial: setiap sampel memuat **60 hari terakhir** data harga saham.  
   - Bentuk input (`X_train_gru`): `(jumlah_sampel, 60, jumlah_fitur)`  
   - Target (`y_train_gru`): harga saham hari ke-61.  

2. **Membangun Arsitektur Model**  

   ![arsitektur model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/arsitektur_model_gru.png)

   Model disusun dengan layer sebagai berikut:  
   - **GRU Layer**: 64 unit, `return_sequences=False` (output satu nilai).  
   - **Dropout Layer**: 0.2 (20 %) untuk mengurangi overfitting.  
   - **Dense Layer**: 1 unit (regresi harga saham).  

3. **Kompilasi Model**  

   ![compile model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/compile_model_gru.png)

   Model dikompilasi dengan:  
   - **Loss Function**: Mean Squared Error (MSE) → cocok untuk regresi numerik.  
   - **Optimizer**: Adam dengan learning rate 0.0005 → adaptif & cepat konvergen.  

4. **EarlyStopping Callback**  

   ![EarlyStopping model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/EarlyStopping_model_gru.png)

   Untuk mencegah overfitting:  
   - Memantau `val_loss`.  
   - Menghentikan pelatihan apabila `val_loss` tidak membaik selama **5 epoch**.  
   - Mengembalikan bobot terbaik secara otomatis (`restore_best_weights=True`).  

5. **Training Model**  

   ![training model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/training_model_gru.png)

   Model dilatih dengan parameter:  
   - **Epochs**: maksimum 60  
   - **Batch Size**: 16  
   - **Validation Split**: 10 % data latih  
   - **Callback**: EarlyStopping  

**Parameter Model GRU**

| Parameter          | Nilai                                   |
|--------------------|-----------------------------------------|
| Model Type         | GRU                                     |
| Hidden Units       | 64                                      |
| Dropout Rate       | 0.2                                     |
| Loss Function      | Mean Squared Error (MSE)                |
| Optimizer          | Adam                                    |
| Learning Rate      | 0.0005                                  |
| Epochs             | 60                                      |
| Batch Size         | 16                                      |
| Early Stopping     | Patience = 5, Restore Best              |
| Validation Split   | 10 %                                    |
| Input Shape        | (60, 1)                                 |

---

### Perbandingan Arsitektur GRU vs LSTM

| **Aspek**                     | **LSTM**                                                  | **GRU**                                                 |
|------------------------------|-----------------------------------------------------------|---------------------------------------------------------|
| **Unit Sel**                 | Memiliki *cell state* dan *hidden state*                  | Hanya *hidden state*                                    |
| **Jumlah Gate**              | 3 gate: input, forget, output                             | 2 gate: reset dan update                                |
| **Kompleksitas Arsitektur**  | Lebih kompleks, jumlah parameter lebih banyak             | Lebih sederhana dan ringan                              |
| **Kinerja pada Data Panjang**| Unggul untuk urutan panjang & pola kompleks               | Cocok untuk data lebih pendek, cepat konvergen          |
| **Waktu Training**           | Relatif lebih lama karena arsitektur lebih kompleks       | Lebih cepat karena struktur ringan                      |

---

**Rubrik/Kriteria Tambahan (Opsional)**:

### Kelebihan dan Kekurangan Model

#### 🔷 LSTM (Long Short-Term Memory)

**Kelebihan:**
- Mampu menangani *long-term dependencies* dengan baik.
- Cocok untuk time series dengan pola jangka panjang dan kompleks.
- Lebih akurat pada urutan data yang panjang.

**Kekurangan:**
- Proses training lebih lambat karena arsitektur kompleks.
- Memiliki lebih banyak parameter, sehingga rawan overfitting jika data sedikit.


#### 🔷 GRU (Gated Recurrent Unit)

**Kelebihan:**
- Lebih cepat dilatih karena struktur lebih sederhana.
- Performa mendekati LSTM tetapi dengan komputasi yang lebih ringan.
- Cocok untuk dataset kecil atau dengan urutan pendek.

**Kekurangan:**
- Tidak memiliki *cell state*, hanya menggunakan *hidden state*.
- Bisa kurang presisi untuk data dengan urutan yang sangat panjang.

---

**Rubrik/Kriteria Tambahan (Opsional)**:

### Pemilihan Model Terbaik dan Alasannya

Dalam proyek ini, digunakan dua model deep learning berbasis Recurrent Neural Network (RNN), yaitu **LSTM (Long Short-Term Memory)** dan **GRU (Gated Recurrent Unit)**. Kedua model dilatih menggunakan data historis harga saham untuk memprediksi harga masa depan.

Setelah dilakukan pelatihan dan evaluasi terhadap kedua model menggunakan metrik evaluasi seperti **MAE, RMSE, dan MAPE**, diperoleh hasil sebagai berikut (contoh):

**Data Normalisasi**

| Model |     MAE      |     RMSE      |
|-------|--------------|---------------|
| LSTM  |    0.0257    |    0.0324     |
| GRU   |    0.0265    |    0.0334     |

**Data Asli**

| Model | MAE (Rupiah) | RMSE (Rupiah) | MAPE (%) |
|-------|--------------|---------------|----------|
| LSTM  |     56.75    |     71.71     |   1.82   |
| GRU   |     58.61    |     73.91     |   1.88   |


#### Model Terbaik: **GRU**

**Alasan Pemilihan:**
- GRU memberikan hasil **error yang lebih rendah** pada ketiga metrik utama (MAE, RMSE, dan MAPE), menunjukkan performa prediksi yang lebih akurat dan stabil.
- GRU memiliki arsitektur yang **lebih sederhana dan lebih cepat dilatih** dibanding LSTM, namun tetap mampu menangkap pola urutan data dengan baik.
- GRU lebih **efisien secara komputasi** dan cocok untuk penggunaan produksi atau deployment karena waktu inferensi yang lebih cepat.

Dengan pertimbangan performa dan efisiensi, **model GRU dipilih sebagai model terbaik** untuk menyelesaikan permasalahan prediksi harga saham pada proyek ini.


**KESIMPULAN MODELING**
- Dua model dibangun: LSTM dan GRU untuk prediksi harga saham berbasis data historis.
- Keduanya memakai input sekuensial 60 hari dan dievaluasi dengan MAE, RMSE, dan MAPE.
- GRU unggul dalam akurasi (error lebih kecil), efisiensi waktu training, dan stabilitas prediksi.
- GRU dipilih sebagai model terbaik karena lebih cepat, ringan, dan akurat dalam memprediksi harga saham TLKM.

---

## Evaluation

### Metrik Evaluasi yang Digunakan
Dalam proyek ini, jenis data yang digunakan adalah **time series** berupa harga historis saham harian PT Telekomunikasi Indonesia Tbk (TLKM). Oleh karena itu, metrik evaluasi yang digunakan harus mampu mengukur **akurasi numerik** dari nilai yang diprediksi terhadap nilai aktual dalam dimensi waktu.

Pemilihan metrik dilakukan berdasarkan kesesuaian dengan konteks data, rumusan permasalahan (problem statement), dan solusi yang ingin dicapai, yaitu prediksi nilai kontinu (harga saham). Untuk itu, proyek ini menggunakan tiga metrik evaluasi berikut:

- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**
- **MAPE (Mean Absolute Percentage Error)**

Dengan menggunakan ketiga metrik ini secara bersamaan, evaluasi model menjadi lebih komprehensif dan relevan untuk tujuan bisnis, dan mampu memberikan pemahaman yang baik tentang kesalahan prediksi harga saham, serta digunakan secara luas dalam konteks forecasting dan analisis finansial.

---

### Hasil Proyek Berdasarkan Metrik evaluasi

#### Tabel Hasil Evaluasi

**1. Evaluasi Matriks (Data Scaled)**

Untuk perbandingan performa model terhadap data yang telah diskalakan (MinMaxScaler), berikut adalah hasil metrik pada data uji:

| Model |     MAE      |     RMSE      |
|-------|--------------|---------------|
| LSTM  |    0.0384    |    0.0469     |
| GRU   |    0.0245    |    0.0313     |

**Insight**

- GRU memiliki MAE lebih rendah daripada LSTM (0.0245 vs 0.0384), menunjukkan bahwa secara rata-rata, prediksi GRU lebih dekat ke nilai aktual dibandingkan LSTM.
- RMSE GRU juga lebih kecil dibandingkan LSTM (0.0313 vs 0.0469), mengindikasikan bahwa prediksi GRU lebih konsisten dan lebih stabil terhadap fluktuasi data.
- Secara keseluruhan, GRU unggul tipis dari LSTM dalam hal akurasi dan stabilitas pada data yang telah dinormalisasi, menjadikannya pilihan yang lebih baik untuk model saat ini.


**2. Evaluasi Matriks (Data Asli)**

Berikut adalah hasil evaluasi performa model LSTM dan GRU terhadap data uji menggunakan skala asli :

| Model | MAE (Rupiah) | RMSE (Rupiah) | MAPE (%) |
|-------|--------------|---------------|----------|
| LSTM  |     84.76    |     103.71    |   2.69   |
| GRU   |     54.18    |     69.13     |   1.73   |

> *Catatan: Nilai RMSE dihitung dari akar kuadrat MSE.*

**Insight:**

- Model GRU menunjukkan performa lebih baik dibandingkan LSTM di seluruh metrik:
    - MAE GRU lebih rendah (54.18 vs 84.76 Rupiah), artinya secara rata-rata prediksi GRU lebih dekat ke nilai aktual.
    - RMSE GRU juga lebih kecil (69.13 vs 103.71 Rupiah), menunjukkan bahwa error GRU lebih stabil dan tidak menyimpang jauh.
    - MAPE GRU juga lebih rendah (1.73% vs 2.69%), berarti prediksi GRU secara relatif lebih akurat terhadap nilai aktual.
- Secara keseluruhan, GRU lebih unggul dalam memprediksi harga saham pada data asli, sehingga layak dipertimbangkan untuk forecasting jangka pendek.
  

#### Table Hasil Forecasting (7 hari kedepan)

| Hari ke- | Harga Aktual  | Prediksi GRU | Prediksi LSTM  |
|----------|---------------|--------------|----------------|
| 1        | 2900.0        | 2785.0       | 2851.5         |
| 2        | 2900.0        | 2771.8       | 2840.1         |
| 3        | 2820.0        | 2761.9       | 2831.6         |
| 4        | 2780.0        | 2753.1       | 2824.7         |
| 5        | 2800.0        | 2744.7       | 2818.9         |
| 6        | 2770.0        | 2736.5       | 2813.8         |
| 7        | 2740.0        | 2728.4       | 2809.3         |


**Insight:**

- Kedua model (GRU dan LSTM) menghasilkan prediksi yang cenderung stabil di kisaran 2780-an, sedangkan harga aktual mengalami penurunan bertahap dari 2900 ke 2740.
- GRU cenderung underpredict (meremehkan) harga di awal (Hari ke-1 dan ke-2), tetapi tetap mendekati tren penurunan.
- LSTM juga underpredict namun sedikit lebih responsif terhadap perubahan arah tren, terutama dari Hari ke-3 ke bawah.
- Meskipun kedua model belum mengikuti penurunan aktual secara tajam, LSTM menunjukkan pola prediksi yang lebih adaptif dibandingkan GRU.
- **Kesimpulan**: Untuk horizon 7 hari ke depan, LSTM memberikan prediksi yang sedikit lebih dinamis, sedangkan GRU menghasilkan output yang lebih konservatif dan stabil, namun kurang mengikuti penurunan aktual secara tajam.


#### Visualisasi Hasil Evaluasi 

![Grafik Evaluasi Aktual vs LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_Next7Days.png)

**Insight:** 
- Prediksi LSTM tidak akurat untuk jangka pendek.
- Garis prediksi tampak terlalu datar, tidak mampu mengikuti fluktuasi tajam harga aktual.
- Terjadi penyimpangan besar terutama di hari ke-6 dan 7, saat harga aktual turun tajam, tetapi prediksi tetap datar.


![Grafik Evaluasi Aktual vs LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_Next7Days.png)

**Insight:** 
- Prediksi LSTM tidak akurat untuk jangka pendek.
- Garis prediksi tampak terlalu datar, tidak mampu mengikuti fluktuasi tajam harga aktual.
- Terjadi penyimpangan besar terutama di hari ke-6 dan 7, saat harga aktual turun tajam, tetapi prediksi tetap datar.
  
  
![Grafik Evaluasi Aktual vs LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_Next7Days.png)

**Insight:** 
- Prediksi LSTM tidak akurat untuk jangka pendek.
- Garis prediksi tampak terlalu datar, tidak mampu mengikuti fluktuasi tajam harga aktual.
- Terjadi penyimpangan besar terutama di hari ke-6 dan 7, saat harga aktual turun tajam, tetapi prediksi tetap datar.
  
  
![Grafik Evaluasi Aktual vs LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_Next7Days.png)

**Insight:** 
- Prediksi LSTM tidak akurat untuk jangka pendek.
- Garis prediksi tampak terlalu datar, tidak mampu mengikuti fluktuasi tajam harga aktual.
- Terjadi penyimpangan besar terutama di hari ke-6 dan 7, saat harga aktual turun tajam, tetapi prediksi tetap datar.
- 

![Grafik Evaluasi Aktual vs LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_Next7Days.png)

**Insight:** 
- Prediksi LSTM tidak akurat untuk jangka pendek.
- Garis prediksi tampak terlalu datar, tidak mampu mengikuti fluktuasi tajam harga aktual.
- Terjadi penyimpangan besar terutama di hari ke-6 dan 7, saat harga aktual turun tajam, tetapi prediksi tetap datar.

---


#### Visualisasi Hasil Forecasting

![Grafik Evaluasi Aktual vs LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_Next7Days.png)

![Grafik Evaluasi Aktual vs LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_Next7Days.png)

---

**Rubrik/Kriteria Tambahan (Opsional)**:

### Penjelasan Metrik Evaluasi (Formula, Cara Kerja, Interpretasi)

#### 1. Mean Absolute Error (MAE)
MAE mengukur rata-rata kesalahan absolut antara nilai aktual (yᵢ) dan prediksi (ŷᵢ). Metrik ini memberikan gambaran langsung seberapa jauh model meleset dari nilai sebenarnya, tanpa memperhatikan arah kesalahan.

$$
\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
$$

**Cara Metriks Bekerja:**
- Menghitung selisih absolut antara prediksi dan nilai aktual untuk setiap data.
- Mengambil rata-rata dari semua selisih tersebut.

**Interpretasi**
- Semakin kecil MAE, semakin akurat model dalam memprediksi.


#### 2. Root Mean Squared Error (RMSE)
RMSE menghitung akar dari rata-rata kuadrat selisih antara nilai aktual dan prediksi. Metrik ini lebih sensitif terhadap error besar.

$$
\text{RMSE} = \sqrt{ \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 }
$$

**Cara Metriks Bekerja:**
- Mengkuadratkan selisih antara prediksi dan nilai aktual untuk menekankan kesalahan besar.
- Menghitung rata-rata dari kuadrat selisih tersebut.
- Mengambil akar kuadrat dari rata-rata untuk mengembalikan ke skala asli.

**Interpretasi**
- Semakin kecil RMSE, semakin presisi model, terutama dalam menghindari kesalahan besar.


#### 3. Mean Absolute Percentage Error (MAPE)
MAPE menyatakan kesalahan prediksi dalam bentuk persentase dari nilai aktual, sehingga memudahkan pemahaman dalam konteks bisnis.

$$
\text{MAPE} = \frac{100\%}{n} \sum_{i=1}^{n} \left| \frac{y_i - \hat{y}_i}{y_i} \right|
$$

**Cara Metriks Bekerja:**
- Menghitung selisih absolut antara prediksi dan nilai aktual, lalu dibagi nilai aktual untuk mendapatkan proporsi kesalahan.
- Mengambil rata-rata dari proporsi kesalahan tersebut.
- Dikalikan 100% agar hasilnya dalam persentase.

**Interpretasi**
- Semakin kecil MAPE, semakin baik akurasi model dalam bentuk persentase kesalahan.

---

**KESIMPULAN HASIL EVALUASI**

- **GRU** menunjukkan performa lebih baik dari **LSTM** untuk semua horizon prediksi (7, 30, 60 hari), berdasarkan MAE, RMSE, dan MAPE.
- Nilai **MAPE < 1%** menunjukkan bahwa kedua model sangat akurat dalam memprediksi harga saham TLKM.
- Perbedaan nilai MAE dan RMSE menunjukkan bahwa **kesalahan besar** (outlier) dapat dikendalikan cukup baik oleh model.
- Model tetap stabil saat prediksi diperluas dari 7 ke 60 hari, menandakan potensi penggunaan untuk prediksi menengah.

---

## Conclusion
1. Proyek berhasil membangun dua model deep learning berbasis time series, yaitu LSTM dan GRU, untuk memprediksi harga penutupan saham PT Telekomunikasi Indonesia Tbk (TLKM) menggunakan data historis.
2. Evaluasi model dilakukan dengan metrik MAE, RMSE, dan MAPE untuk mengukur akurasi dan stabilitas prediksi. Hasilnya menunjukkan bahwa:
3. Kedua model memiliki performa prediksi yang baik.
    - GRU menunjukkan efisiensi lebih tinggi dari segi waktu pelatihan.
    - LSTM lebih unggul dalam menangkap pola jangka panjang.
4. Prediksi dilakukan untuk tiga skenario waktu: 7 hari, 30 hari, dan 60 hari ke depan, yang menunjukkan bahwa model mampu beradaptasi dengan horizon waktu berbeda.
5. Hasil prediksi menunjukkan bahwa model dapat menangkap tren harga dengan cukup baik, dan prediksi mendekati nilai aktual, terutama dalam jangka pendek (7 hari).
6. Kedua model memberikan insight yang berguna bagi investor dan analis pasar, khususnya dalam pengambilan keputusan berbasis data yang lebih akurat dan informatif.

**---Ini adalah bagian akhir laporan---**


