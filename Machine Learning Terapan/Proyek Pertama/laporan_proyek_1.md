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
5. Melakukan eksperimen prediksi harga penutupan saham TLKM untuk 7 hari ke depan
  
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

Untuk menyelesaikan permasalahan prediksi harga saham TLKM secara akurat, dua algoritma deep learning berbasis Recurrent Neural Network (RNN) digunakan sebagai solusi utama:

**1. Long Short-Term Memory (LSTM)**
LSTM dirancang untuk mengatasi permasalahan long-term dependency pada data deret waktu. Algoritma ini menggunakan empat gerbang (input, forget, output, dan cell state) yang memungkinkan model mempertahankan informasi penting dari data historis harga saham untuk membuat prediksi yang lebih akurat.

**2. Gated Recurrent Unit (GRU)**
GRU adalah versi yang lebih ringan dari LSTM dengan hanya dua gerbang (update dan reset). Algoritma ini lebih efisien secara komputasi dan cocok untuk dataset dengan kompleksitas sedang, dengan tetap mampu menangkap pola temporal yang relevan untuk prediksi harga saham jangka pendek.

Kedua algoritma tersebut dibandingkan performanya dalam konteks forecasting harga saham 7 hari ke depan untuk menentukan model terbaik berdasarkan evaluasi metrik seperti MAE, RMSE, dan MAPE.

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
   
***Jumlah Outlier per Kolom (Metode IQR)**

| No | Kolom      | Jumlah Outlier |
|----|------------|----------------|
| 1  | Adj Close  | 0              |
| 2  | Close      | 0              |
| 3  | High       | 0              |
| 4  | Low        | 0              |
| 5  | Open       | 0              |
| 6  | Volume     | 64             |

##### 1. Outlier pada Data Volume Asli

**Visualisasi Outlier Sebelum Penanganan**

- Boxplot Outlier Volume  
  ![BoxPlot Outlier Volume](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/BoxPlot_Outlier_Volume.png)

- Scatterplot Volume Sebelum Penanganan  
  ![ScatterPlot Outlier Volume Before](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/ScatterPlot_Outlier_Volume_Before.png)

Titik merah pada scatterplot menandai data yang terdeteksi sebagai outlier karena berada jauh di atas mayoritas nilai volume lainnya.


### Penanganan Outlier dengan Transformasi Logaritmik

Karena distribusi volume sangat condong ke kanan (positively skewed), dilakukan transformasi logaritmik natural (`log1p`) untuk menormalkan distribusi:

\[
Volume_{log} = \log(Volume + 1)
\]

Setelah transformasi, dilakukan kembali deteksi outlier dengan metode IQR terhadap kolom `Volume_log`.


**Visualisasi Outlier Setelah Transformasi**

- Scatterplot Volume Setelah Transformasi Log  
  ![ScatterPlot Outlier Volume After](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/ScatterPlot_Outlier_Volume_After.png)

Setelah transformasi logaritmik, jumlah outlier berkurang signifikan dan sebaran data menjadi lebih seragam.


**Insight dari Visualisasi**

- Data volume saham TLKM memiliki distribusi yang tidak normal dan mengandung sejumlah outlier signifikan.
- Deteksi awal menunjukkan adanya outlier dengan nilai volume yang sangat besar.
- Dengan menerapkan transformasi logaritmik, distribusi menjadi lebih seimbang dan jumlah outlier berkurang.
- Pendekatan ini mempertahankan seluruh data sambil meminimalkan pengaruh nilai ekstrem terhadap analisis.


---


##### 2. Outlier pada Harga Close Berdasarkan Waktu

Berikut adalah daftar waktu (berdasarkan kombinasi tahun dan bulan) di mana **nilai `Close` terdeteksi sebagai outlier**:

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

**Catatan penting**:
> Ini berarti bahwa dalam bulan dan tahun yang disebutkan, terdapat nilai `Close` yang secara statistik terdeteksi sebagai outlier. Nilai tersebut menyimpang dari distribusi harga normal di bulan tersebut.


**Penanganan Outlier dengan Metode Capping**

- Nilai `Close` yang lebih kecil dari `Lower Bound` digantikan dengan batas bawah.
- Nilai `Close` yang lebih besar dari `Upper Bound` digantikan dengan batas atas.

Tujuan dari capping ini adalah **menyesuaikan nilai ekstrim tanpa membuang data**.


**Visualisasi: Sebelum vs Sesudah Penanganan Outlier**

![LinePlot Outlier Before vs After](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/LinePlot_Oulier_Before_vs_After.png)

**Penjelasan grafik:**
- Garis **biru**: nilai `Close` **sebelum penanganan**, tampak banyak titik merah (outlier).
- Garis **oranye**: nilai `Close_Capped` **setelah penanganan**, lebih halus dan stabil.
- **Titik merah** menghilang setelah proses capping, menandakan bahwa outlier telah diatasi.


**Insight dari Visualisasi**

- Outlier terdeteksi di banyak titik antara tahun 2020 hingga 2024.
- Paling banyak terjadi pada tahun 2021 dan 2023.
- Setelah penanganan, grafik menunjukkan tren yang lebih realistis dan bebas gangguan titik ekstrem.
- Ini membuat data lebih akurat untuk analisis lanjutan dan pemodelan machine learning.


---


![LinePlot Distribuasi Date](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/LinePlot_Distribuasi_Date.png)

**Penjelasan:**

Grafik ini menunjukkan distribusi data berdasarkan tanggal, dengan asumsi satu data per hari.

**Insight:**

- Data tersebar merata sepanjang waktu, tanpa adanya hari kosong atau gap yang signifikan.
- Ini menunjukkan bahwa data dikumpulkan secara teratur dan konsisten dalam konteks time-series.
- Distribusi yang stabil ini sangat penting untuk pelatihan model LSTM, karena model akan belajar dari urutan waktu yang berkesinambungan.
- Konsistensi juga membantu model mengenali pola tren dan musiman dengan lebih baik.


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
Data preparation merupakan tahap penting yang menjembatani proses data understanding dengan modeling. Kualitas dan ketepatan pada tahap ini akan sangat berpengaruh terhadap performa akhir model. Dalam proyek ini, data preparation dilakukan melalui beberapa tahap terstruktur berikut:

---

### 1. Menyalin Data Awal ke Variabel Baru

**Proses:**  
Dataset awal hasil pembersihan (`df_clean`) disalin ke dalam variabel baru (`df_final`) untuk memastikan data asli tetap aman dari perubahan yang mungkin terjadi pada proses selanjutnya.

**Alasan:**  
Praktik ini penting untuk menjaga *data integrity*. Jika terjadi kesalahan pada transformasi berikutnya, kita masih memiliki versi bersih yang bisa digunakan kembali tanpa perlu mengulang proses dari awal. Ini juga meningkatkan efisiensi saat iterasi model.

---

### 2. Feature Engineering: Ekstraksi Fitur Date

**Proses:**  
Dari kolom `Date`, diekstrak tiga fitur baru yaitu:
- `Year` (tahun),
- `Month` (bulan), dan
- `Day` (tanggal).

Setelah itu, kolom `Date` dihapus karena tidak dibutuhkan lagi dalam format datetime.

**Alasan:**  
Model machine learning, termasuk LSTM dan GRU, tidak dapat secara langsung memahami konteks waktu dari format tanggal. Dengan mengubah `Date` menjadi fitur numerik seperti tahun, bulan, dan hari, kita membantu model mengenali pola temporal, seperti musiman atau tren tahunan.  
Menghapus kolom `Date` diperlukan karena tipe data datetime tidak dapat diolah secara langsung oleh model numerik tanpa diubah menjadi representasi angka yang bermakna.

---

### 2. Feature Engineering: Ekstraksi Komponen Waktu

**Proses:**

- Dari kolom `Date`, tiga fitur waktu utama diekstraksi:
  - `Year` (tahun),
  - `Month` (bulan),
  - `Day` (tanggal).
- Setelah ekstraksi selesai, kolom `Date` dihapus dari dataframe karena informasinya sudah terdistribusi dalam tiga fitur baru.

**Alasan:**

Ekstraksi waktu dilakukan karena elemen waktu merupakan salah satu faktor kunci dalam pemodelan data deret waktu (time-series). Dengan menguraikan `Date` menjadi `Year`, `Month`, dan `Day`, model memiliki konteks temporal eksplisit yang memungkinkan pembelajaran pola musiman, tren tahunan, atau efek harian. Ini sangat krusial dalam memprediksi harga atau perilaku data yang berubah terhadap waktu.


---


### 3. Data Splitting dan Normalisasi

**Proses:**

1. **Pemilihan Fitur dan Target**
   - Fitur yang digunakan untuk pelatihan adalah `Open`, `High`, dan `Low`.
   - Target yang akan diprediksi adalah `Close_Capped` (harga penutupan yang telah dikap).

2. **Pemisahan Data Berdasarkan Waktu**
   - Data dibagi menjadi dua subset:
     - **Training set**: 80% pertama dari data secara kronologis.
     - **Testing set**: 20% sisanya.
   - Pembagian ini **tidak dilakukan secara acak (no shuffle)** untuk menjaga urutan waktu agar konteks historis tetap terpelihara.

3. **Normalisasi (Min-Max Scaling)**
   - Fitur dan target dalam training set dilakukan **fit dan transform** menggunakan `MinMaxScaler`.
   - Data testing hanya di-**transform** menggunakan skala dari data training (tanpa fit ulang) untuk menghindari data leakage.

**Alasan:**

- **Pemisahan data** secara waktu sangat penting dalam masalah time-series. Jika data diacak, model bisa mempelajari informasi dari masa depan yang seharusnya tidak diketahui saat pelatihan, sehingga menghasilkan estimasi performa yang tidak realistis.
- **Normalisasi** diperlukan karena algoritma deep learning sensitif terhadap skala fitur. Jika rentang nilai berbeda-beda (misalnya `Open` ratusan dan `Low` puluhan), maka proses pembelajaran akan tidak seimbang. MinMaxScaler mengubah semua fitur ke skala yang sama (0–1), mempercepat konvergensi, dan meningkatkan stabilitas pelatihan.
- **Transformasi hanya pada data test** mencegah kebocoran informasi dari data uji ke pelatihan yang bisa membuat model tampak lebih baik dari kenyataannya.

---

### 4. Pembentukan Sequence (Time Series Windowing)

**Proses:**

- Data diubah menjadi bentuk urutan (sequence) agar sesuai dengan format input model LSTM atau GRU.
- Setiap sampel input (`X`) dibentuk dari 60 langkah waktu sebelumnya. Misalnya, `X[60]` berisi data dari waktu ke-0 hingga ke-59, dan targetnya adalah `y[60]`.
- Fungsi `create_sequences` membentuk pasangan input-output dalam bentuk array tiga dimensi:
  - `X_train_seq`: `(jumlah sample, 60, 3)` — 60 langkah, 3 fitur.
  - `y_train_seq`: `(jumlah sample, 1)` — target yang sesuai.
  - Hal yang sama dilakukan pada data testing.

**Alasan:**

Model seperti LSTM, GRU, dan arsitektur time-series lainnya tidak bekerja dengan data tabular biasa, tetapi membutuhkan input dalam bentuk urutan agar dapat mengenali pola historis. Tanpa pembentukan sequence ini, model tidak akan dapat memahami dinamika waktu yang merupakan inti dari masalah prediksi dalam deret waktu. Jumlah langkah waktu (60) dipilih berdasarkan eksperimen dan representasi konteks temporal yang cukup panjang.

---

### ✅ Struktur Output Akhir

Setelah semua tahap preparation selesai, struktur akhir data adalah sebagai berikut:

| Dataset       | Shape (Contoh)             |
|---------------|-----------------------------|
| X_train_seq   | (936, 60, 3)                |
| y_train_seq   | (936, 1)                    |
| X_test_seq    | (234, 60, 3)                |
| y_test_seq    | (234, 1)                    |


---


## Modeling

Tahapan ini menjelaskan proses pembangunan dua model Deep Learning, yaitu **LSTM** dan **GRU**, untuk memprediksi harga saham menggunakan data historis.

### Model 1: LSTM (Long Short-Term Memory)

**Tahapan Pemodelan**
1. Persiapan Data Input
    - Data disusun dalam bentuk sekuensial untuk memodelkan pola deret waktu (time series).
    - Setiap sampel input merepresentasikan 60 hari terakhir dari tiga fitur harga saham: Open, High, dan Low.
    - Bentuk input (X_train_seq): (jumlah_sampel, 60, 3), di mana 3 adalah jumlah fitur.
    - Target (y_train_seq): harga Close_Capped pada hari ke-61, yang diprediksi berdasarkan urutan 60 hari sebelumnya.
  
2. Membangun Arsitektur Model
   
   ![arsitektur model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/arsitektur_model_lstm.png)

   Model LSTM dibangun dengan susunan layer berikut:
   - LSTM Layer: 64 unit dengan return_sequences=False, artinya hanya menghasilkan satu output (prediksi untuk satu waktu).
   - Dropout Layer: 0.2 (20%) untuk mengurangi risiko overfitting dengan menonaktifkan sebagian neuron saat training.
   - Dense Layer: 1 unit output sebagai hasil prediksi harga
  
4. Kompilasi Model

   ![compile model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/compile_model_ltsm.png)
   
   Model dikompilasi menggunakan:  
   - Loss Function: Mean Squared Error (MSE) — metrik umum untuk regresi yang mengukur rata-rata kuadrat dari selisih antara nilai aktual dan prediksi.
   - Optimizer: Adam dengan learning_rate = 0.0005 — optimizer yang adaptif dan efisien untuk model deep learning.  
  
5. EarlyStopping Callback
   
   ![EarlyStopping model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/EarlyStopping_model_lstm.png)

   Digunakan untuk mencegah overfitting selama training dengan ketentuan:  
   - Memantau nilai val_loss (validasi).
   - Jika tidak terjadi peningkatan selama 5 epoch berturut-turut, proses pelatihan dihentikan.
   - Opsi restore_best_weights=True memastikan model mengembalikan bobot terbaik (dengan val_loss terendah).

6. Training Model

   ![training model lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/training_model_lstm.png)
   
   Model dilatih dengan parameter:  
   - Epochs: maksimum 60 iterasi pelatihan.
   - Batch Size: 16 (jumlah data dalam satu mini-batch).
   - Validation Split: 10% dari data pelatihan digunakan sebagai data validasi.
   - Callback: EarlyStopping digunakan untuk mengontrol proses pelatihan.

**Parameter Model**

![model summary lstm](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/model_summary_lstm.png)

- LSTM Layer: Terdiri dari 64 unit dengan total 17.408 parameter, menjadikan LSTM lebih kompleks dari GRU karena 4 gerbang internal (forget, input, candidate, output).
- Dropout Layer: Tidak memiliki parameter, digunakan untuk mengurangi overfitting, dan meneruskan 64 output dari layer sebelumnya dengan beberapa unit dinonaktifkan (drop) secara acak saat training.
- Dense Layer: Menerima input dari 64 unit sebelumnya dan menghasilkan 1 output prediksi dengan total 65 parameter (64 bobot + 1 bias).


| Parameter             | Nilai                         |
|-----------------------|-------------------------------|
| Model Type            | LSTM                          |
| Hidden Units          | 64                            |
| Dropout Rate          | 0.2                           |
| Loss Function         | Mean Squared Error (MSE)      |
| Optimizer             | Adam                          |
| Learning Rate         | 0.0005                        |
| Epochs                | 100                            |
| Batch Size            | 16                            |
| Early Stopping        | Patience = 5, Restore Best    |
| Validation Split      | 10%                           |
| Input Shape           | (60, 3)                       |

---

### Model 2: GRU (Gated Recurrent Unit)

**Tahapan Pemodelan**

1. **Persiapan Data Input**  
    - Data disusun dalam bentuk sekuensial untuk memodelkan pola deret waktu (time series).
    - Setiap sampel input merepresentasikan 60 hari terakhir dari tiga fitur harga saham: Open, High, dan Low.
    - Bentuk input (X_train_seq): (jumlah_sampel, 60, 3), di mana 3 adalah jumlah fitur.
    - Target (y_train_seq): harga Close_Capped pada hari ke-61, yang diprediksi berdasarkan urutan 60 hari sebelumnya.

2. **Membangun Arsitektur Model**  

   ![arsitektur model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/arsitektur_model_gru.png)

   Model GRU dibangun dengan susunan layer berikut:
   - GRU Layer: 64 unit dengan return_sequences=False, artinya hanya menghasilkan satu output (prediksi untuk satu waktu).
   - Dropout Layer: 0.2 (20%) untuk mengurangi risiko overfitting dengan menonaktifkan sebagian neuron saat training.
   - Dense Layer: 1 unit output sebagai hasil prediksi harga.

3. **Kompilasi Model**  

   ![compile model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/compile_model_gru.png)

   Model dikompilasi menggunakan:  
   - Loss Function: Mean Squared Error (MSE) — metrik umum untuk regresi yang mengukur rata-rata kuadrat dari selisih antara nilai aktual dan prediksi.
   - Optimizer: Adam dengan learning_rate = 0.0005 — optimizer yang adaptif dan efisien untuk model deep learning.  

4. **EarlyStopping Callback**  

   ![EarlyStopping model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/EarlyStopping_model_gru.png)

   Digunakan untuk mencegah overfitting selama training dengan ketentuan:  
   - Memantau nilai val_loss (validasi).
   - Jika tidak terjadi peningkatan selama 5 epoch berturut-turut, proses pelatihan dihentikan.
   - Opsi restore_best_weights=True memastikan model mengembalikan bobot terbaik (dengan val_loss terendah).

5. **Training Model**  

   ![training model gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/training_model_gru.png)

   Model dilatih dengan parameter:  
   - Epochs: maksimum 60 iterasi pelatihan.
   - Batch Size: 16 (jumlah data dalam satu mini-batch).
   - Validation Split: 10% dari data pelatihan digunakan sebagai data validasi.
   - Callback: EarlyStopping digunakan untuk mengontrol proses pelatihan.

**Parameter Model GRU**

![model summary gru](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/model_summary_gru.png)

- GRU Layer: Terdiri dari 64 unit dengan total 13.248 parameter, lebih ringan dari LSTM karena hanya memiliki 3 gerbang internal (reset, update).
- Dropout Layer: Tidak memiliki parameter, digunakan untuk mengurangi overfitting, dan meneruskan 64 output dari layer sebelumnya dengan beberapa unit dinonaktifkan secara acak saat training.
- Dense Layer: Menerima input dari 64 unit sebelumnya dan menghasilkan 1 output prediksi dengan total 65 parameter (64 bobot + 1 bias).

| Parameter          | Nilai                                   |
|--------------------|-----------------------------------------|
| Model Type         | GRU                                     |
| Hidden Units       | 64                                      |
| Dropout Rate       | 0.2                                     |
| Loss Function      | Mean Squared Error (MSE)                |
| Optimizer          | Adam                                    |
| Learning Rate      | 0.0005                                  |
| Epochs             | 100                                      |
| Batch Size         | 16                                      |
| Early Stopping     | Patience = 5, Restore Best              |
| Validation Split   | 10 %                                    |
| Input Shape        | (60, 3)                                 |

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
| LSTM  |    0.0384    |    0.0469     |
| GRU   |    0.0245    |    0.0313     ||

**Data Asli**

| Model | MAE (Rupiah) | RMSE (Rupiah) | MAPE (%) |
|-------|--------------|---------------|----------|
| LSTM  |     84.76    |     103.71    |   2.69   |
| GRU   |     54.18    |     69.13     |   1.73   |


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


#### Visualisasi Hasil Evaluasi 

![Grafik LSTM Training Loss](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_LSTM_Training_Loss.png)

**Insight:** 
- Grafik menunjukkan penurunan training loss dan validation loss secara bertahap, menandakan proses pelatihan berjalan dengan baik.
- Namun, jarak antara training loss dan validation loss mulai melebar di akhir pelatihan, yang mengindikasikan potensi overfitting ringan.
- Model LSTM cenderung terlalu menyesuaikan dengan data pelatihan dan kurang fleksibel saat menghadapi data baru (validasi).
- Ini dapat menjelaskan mengapa prediksi LSTM terlihat terlalu datar dan tidak mengikuti fluktuasi harga yang tajam.


![Grafik GRU Training Loss](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_GRU_Training_Loss.png)

**Insight:** 
- Baik training loss maupun validation loss menurun secara konsisten dan beriringan, menandakan model GRU belajar dengan stabil dan tidak overfitting.
- Perbedaan antara training dan validation loss sangat kecil, menunjukkan generalisasi model yang baik terhadap data baru.
- GRU lebih cepat konvergen dibanding LSTM dan mempertahankan akurasi yang lebih tinggi di data validasi.
- Hal ini memperkuat temuan bahwa GRU lebih efektif untuk prediksi jangka pendek pada data harga saham TLKM.
  
  
![Grafik Evaluasi Aktual vs LSTM GRU1](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_GRU1..png)

**Insight:** 
- Garis prediksi GRU tampak lebih mengikuti pola harga aktual dibandingkan LSTM.
- LSTM menghasilkan garis prediksi yang lebih datar, cenderung mengabaikan fluktuasi harga yang tajam.
- GRU lebih adaptif terhadap tren penurunan pada hari ke-6 dan 7, meskipun belum sepenuhnya tepat.
  
  
![Grafik Evaluasi Aktual vs LSTM GRU2](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Evaluasi_Aktual_vs_LSTM_GRU2..png)

**Insight:** 
- Grafik ini menguatkan bahwa GRU lebih akurat dalam mengikuti arah tren harga aktual.
- LSTM memiliki jeda respons terhadap perubahan mendadak, terutama saat harga mengalami penurunan signifikan.
- Kedua model cenderung memiliki prediksi yang mendekati rata-rata, tetapi GRU lebih fleksibel dalam mengikuti tren aktual.
  

![Grafik Distribusi Eror Prediksi](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_Distribusi_Eror_Prediksis.png)

**Insight:** 
- Distribusi error menunjukkan sebagian besar nilai error berada dekat dengan nol, menandakan prediksi cukup akurat secara umum.
- GRU menghasilkan error yang lebih sempit dan simetris dibandingkan LSTM, mengindikasikan konsistensi model.
- Tidak ada error ekstrem yang dominan, yang berarti model mampu menahan dampak outlier dengan baik.

---


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

Baik model LSTM maupun GRU berhasil mengenali dan mengikuti pola tren penurunan harga saham Telkom selama 7 hari ke depan. Meskipun terdapat selisih nilai absolut dibandingkan harga aktual, arah pergerakan harga yang diprediksi kedua model sejalan dengan kenyataan — yaitu penurunan bertahap dari hari ke hari.
    - Model tidak hanya menghafal data historis, tapi mampu menangkap pola tren menurun secara konsisten.
    - Model GRU menghasilkan prediksi yang lebih tajam dan stabil, sedangkan LSTM memberikan hasil yang lebih moderat namun tetap mengikuti arah yang sama.
    - Hal ini menunjukkan bahwa kedua model cukup andal dalam memahami pola pergerakan harga, yang merupakan aspek penting dalam forecasting saham berbasis tren.
    

#### Visualisasi Hasil Forecasting

![Grafik GRU Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_GRU_Next7Days.png)

![Grafik LSTM Next7Days](https://raw.githubusercontent.com/2209106126-azahrinathirah/Submission-Coding-Camp/main/Machine%20Learning%20Terapan/Proyek%20Pertama/images/Grafik_LSTM_Next7Days.png)

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

- GRU menunjukkan performa lebih baik dibandingkan LSTM berdasarkan nilai MAE, RMSE, dan MAPE.
- Nilai MAPE < 10% pada kedua model menunjukkan bahwa model memiliki tingkat akurasi yang sangat baik dalam memprediksi harga saham TLKM.
- Perbedaan antara nilai MAE dan RMSE mengindikasikan bahwa kesalahan besar (outlier) dapat dikendalikan dengan cukup baik.
- Model GRU lebih konsisten dalam mengikuti arah tren harga aktual, meskipun harga prediksi sedikit lebih rendah. LSTM juga mengikuti pola, tetapi cenderung memiliki fluktuasi lebih tinggi.
- Secara keseluruhan, model GRU memberikan hasil yang lebih stabil dan presisi, cocok untuk digunakan dalam forecasting jangka pendek.

---

## Conclusion

1. Proyek ini berhasil membangun dua model deep learning berbasis time series dan forecasting, yaitu LSTM dan GRU, untuk memprediksi harga penutupan saham PT Telekomunikasi Indonesia Tbk (TLKM) menggunakan data historis.
2. Evaluasi dilakukan dengan menggunakan metrik MAE, RMSE, dan MAPE untuk mengukur tingkat akurasi dan kestabilan hasil prediksi. Hasil evaluasi menunjukkan bahwa:
    - Kedua model memiliki performa yang baik, dengan MAPE < 10%, yang menunjukkan tingkat akurasi sangat tinggi untuk prediksi harga saham.
    - GRU menunjukkan hasil prediksi yang lebih stabil dan akurat dibandingkan LSTM, serta lebih efisien dari segi waktu pelatihan.
    - Sementara itu, LSTM tetap unggul dalam menangkap pola jangka panjang, meskipun prediksinya lebih fluktuatif dalam jangka pendek.
3. Prediksi dilakukan untuk horizon waktu 7 hari ke depan, dan hasilnya menunjukkan bahwa model mampu mengikuti arah tren harga aktual secara konsisten.
4. Kesimpulannya, kedua model dapat memberikan insight yang bermanfaat bagi investor dan analis pasar, terutama dalam mendukung pengambilan keputusan berbasis data yang lebih akurat dan terukur.

**---Ini adalah bagian akhir laporan---**


