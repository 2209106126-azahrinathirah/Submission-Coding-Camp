# Laporan Proyek Machine Learning - Andi Zahrina Athirah Ahmad

## Domain Proyek
---
**Latar Belakang**
Prediksi harga saham merupakan tantangan penting dalam dunia keuangan, khususnya di pasar modal Indonesia yang terus berkembang pesat dalam beberapa dekade terakhir. Fluktuasi harga saham yang tinggi disebabkan oleh berbagai faktor seperti kondisi ekonomi makro, kinerja perusahaan, sentimen pelaku pasar, serta situasi geopolitik, menjadikan investasi di pasar saham penuh risiko <a href="#1">[1]</a>. Ketidakstabilan ini menyulitkan investor dalam mengambil keputusan yang optimal, terutama untuk jangka menengah dan panjang. Oleh karena itu, dibutuhkan pendekatan prediktif yang mampu mengenali pola-pola kompleks dalam data historis harga saham guna mendukung pengambilan keputusan yang lebih akurat dan berbasis data <a href="#1">[1]</a>.

Salah satu saham yang menarik untuk dianalisis adalah PT Telekomunikasi Indonesia Tbk (TLKM), sebuah perusahaan telekomunikasi milik negara yang termasuk dalam kategori saham blue chip. Saham TLKM aktif diperdagangkan di Bursa Efek Indonesia (BEI) dan memiliki pengaruh besar terhadap indeks utama seperti IHSG dan LQ45 <a href="#2">[2]</a>. Kemampuan untuk memprediksi harga penutupan saham TLKM secara akurat dapat membantu investor, analis pasar, dan pembuat kebijakan dalam membuat keputusan yang lebih rasional dan berbasis data.

Model statistik tradisional seperti ARIMA atau regresi linear sering kali tidak mampu menangkap pola nonlinier dan dependensi jangka panjang dalam data time series saham <a href="#3">[3]</a>. Untuk menjawab tantangan tersebut, pendekatan berbasis deep learning seperti Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) menjadi solusi yang menjanjikan karena kemampuannya dalam mempelajari urutan data historis dan mengingat informasi jangka panjang <a href="#4">[4]</a>.

Melalui proyek ini, saya mengembangkan dan membandingkan model LSTM dan GRU untuk memprediksi harga penutupan saham TLKM, dengan fokus pada tiga skenario waktu ke depan: 7 hari, 30 hari, dan 60 hari. Evaluasi dilakukan menggunakan metrik MAE, RMSE, dan MAPE untuk menilai sejauh mana model dapat memberikan hasil prediksi yang akurat dan stabil <a href="#5">[5]</a>.
    
**Rubrik/Kriteria Tambahan (Opsional)**:

**Mengapa Masalah Ini Harus Diselesaikan❓**
1. Fluktuasi harga saham TLKM yang tinggi membuat investor membutuhkan strategi prediktif berbasis data untuk memaksimalkan return dan meminimalkan risiko.
2. Model statistik konvensional seperti ARIMA atau regresi linear belum mampu menangani data saham yang kompleks, nonlinier, dan bergantung pada urutan waktu.
3. Di era digital, pengambilan keputusan finansial berbasis data dan kecerdasan buatan telah menjadi praktik umum secara global, dan perlu lebih banyak diterapkan di pasar saham Indonesia.

**Bagaimana Masalah Ini Harus Diselesaikan❓**
1. Mengumpulkan data historis harga saham TLKM dari sumber resmi seperti Yahoo Finance atau Bursa Efek Indonesia.
2. Melakukan preprocessing data time series, termasuk normalisasi dan pembuatan window sekuensial.
3. Membangun dua model deep learning: Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) untuk mempelajari pola historis.
4. Mengevaluasi performa model menggunakan metrik MAE, RMSE, dan MAPE untuk mengukur akurasi prediksi.
5. Melakukan eksperimen prediksi harga penutupan saham TLKM untuk tiga horizon waktu ke depan:
   - 7 hari (jangka pendek)
   - 30 hari (jangka menengah)
   - 60 hari (jangka panjang)

## Hasil Riset Terkait (Referensi)

<a name="1">[1]</a> T. Prasetyo dan M. Faisal, *Penerapan Data Mining dalam Prediksi Harga Saham di Indonesia Menggunakan Algoritma LSTM*, IJCIT, vol. 4, no. 2, pp. 116–120, 2019.  
[https://doi.org/10.31294/ijcit.v4i2.7712](https://doi.org/10.31294/ijcit.v4i2.7712)

<a name="2">[2]</a> H. K. Alfredo, *Analysis of Fama and French 3-Factor Model Variables in the Formation of Expected Stock Returns (Issuers of LQ-45 Index Member Stocks for the Period 2020–2022)*, Edunity, vol. 2, no. 7, 2023.  
[https://doi.org/10.57096/edunity.v2i7.122](https://doi.org/10.57096/edunity.v2i7.122)

<a name="3">[3]</a> M. Ridwan et al., *Comparison of ARIMA and GRU Models for High-Frequency Time Series Forecasting*, Scientific Journal of Informatics, vol. 10, no. 3, 2023.  
[https://doi.org/10.15294/sji.v10i3.45965](https://doi.org/10.15294/sji.v10i3.45965)

<a name="4">[4]</a> R. Yavasani dan F. Wang, *Comparative Analysis of LSTM, GRU, and ARIMA Models for Stock Market Price Prediction*, Journal of Student Research, vol. 12, no. 4, 2023.  
[https://doi.org/10.47611/jsrhs.v12i4.5888](https://doi.org/10.47611/jsrhs.v12i4.5888)

<a name="5">[5]</a> N. A. Nilsen, *Perbandingan Model RNN, Model LSTM, dan Model GRU dalam Memprediksi Harga Saham-Saham LQ45*, Jurnal Statistika dan Aplikasinya, vol. 6, no. 1, 2022.  
[https://doi.org/10.21009/JSA.06113](https://doi.org/10.21009/JSA.06113)


## Business Understanding

### Problem Statements

Berdasarkan latar belakang, proyek ini difokuskan untuk menjawab pertanyaan-pertanyaan berikut:

1. Bagaimana membangun model machine learning berbasis deep learning yang mampu memprediksi harga penutupan saham secara akurat berdasarkan data historis?
2. Apakah model Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) dapat memberikan hasil prediksi yang lebih baik dibandingkan pendekatan statistik konvensional seperti ARIMA?
3. Seberapa akurat model yang dibangun dalam memprediksi harga penutupan saham PT Telekomunikasi Indonesia Tbk (TLKM) untuk horizon waktu 7 hari, 30 hari, dan 60 hari ke depan?

### Goals

Tujuan utama dari proyek ini meliputi:

- Mengembangkan dan membandingkan dua model deep learning (LSTM dan GRU) untuk memprediksi harga saham TLKM berdasarkan data historis.
- Menilai performa prediksi dari masing-masing model dengan menggunakan metrik evaluasi MAE (Mean Absolute Error), RMSE (Root Mean Square Error), dan MAPE (Mean Absolute Percentage Error).
- Memberikan insight kepada investor atau analis pasar terhadap akurasi dan stabilitas model prediksi untuk pengambilan keputusan yang lebih informatif.


**Rubrik/Kriteria Tambahan (Opsional)**:

### Solution statements

Untuk mencapai tujuan di atas secara terukur dan optimal, dua pendekatan utama akan dilakukan:

1. **Perbandingan Model Deep Learning**  
   Membangun dua model prediksi berbasis jaringan saraf berulang (RNN):
   - **Long Short-Term Memory (LSTM)**
   - **Gated Recurrent Unit (GRU)**  
   Model dilatih dengan data harga historis saham TLKM dan diuji berdasarkan tiga skenario horizon waktu prediksi: 7 hari, 30 hari, dan 60 hari.

2. **Evaluasi dan Optimasi Model**  
   Evaluasi dilakukan terhadap performa model dengan metrik:
   - **MAE** – Rata-rata kesalahan absolut.
   - **RMSE** – Akar dari rata-rata kuadrat error.
   - **MAPE** – Persentase kesalahan absolut rata-rata.

   Model terbaik kemudian dapat dioptimalkan melalui:
   - **Tuning jumlah neuron, batch size, dan learning rate**
   - **Eksperimen jumlah timestep/input window**  
   untuk meningkatkan stabilitas dan akurasi prediksi.

## Data Understanding

### Deskripsi Dataset

Dataset yang digunakan dalam proyek ini adalah data historis harga saham PT Telekomunikasi Indonesia Tbk (TLKM) yang diperoleh dari situs resmi Yahoo Finance. Data mencakup periode harian dari tahun 2016 hingga 2023, dan terdiri dari informasi harga saham yang biasa digunakan dalam analisis teknikal.

🔗 **Sumber Data:**  
[Dataset Saham Bursa Efek - Kaggle (oleh Agung Pambudi)](https://www.kaggle.com/datasets/agungpambudi/dataset-saham-bursa-efek/data)

Dataset ini berisi total **1212 baris data** harian dengan 7 kolom (fitur utama), dan tidak mengandung nilai duplikat maupun missing value pada kolom waktu maupun harga utama. Data ini digunakan untuk membangun model prediksi time series dan forecasting.

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


**Rubrik/Kriteria Tambahan (Opsional)**:

### Exploratory Data Analysis (EDA)

Beberapa langkah EDA dilakukan untuk memahami pola dan struktur data, antara lain:

1. **EDA - Deskripsi Variable**

Dataset ini terdiri dari **1212 baris data** harian dan **7 kolom** utama dengan tipe data sebagai berikut:

| **No.** | **Fitur**     | **Tipe Data** |
|--------:|---------------|---------------|
| 1       | Date          | object        |
| 2       | Adj Close     | float64       |
| 3       | Close         | float64       |
| 4       | High          | float64       |
| 5       | Low           | float64       |
| 6       | Open          | float64       |
| 7       | Volume        | object        |

**Penjelasan**

- Seluruh kolom numerik (`Adj Close`, `Close`, `High`, `Low`, `Open`) sudah memiliki format data yang sesuai (float64).
- Kolom `Date` dan `Volume` masih bertipe **object**.
  - `Date` perlu dikonversi ke tipe data **datetime** untuk memungkinkan analisis berbasis waktu, seperti tren musiman atau harian.
  - `Volume` perlu dikonversi ke format **numerik** agar dapat dianalisis lebih lanjut, termasuk dalam perhitungan statistik dan visualisasi.
- Tidak terdapat nilai kosong (null) pada seluruh kolom, sehingga data ini siap untuk dianalisis setelah beberapa tahapan transformasi awal.

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

**Penjelasan**

Dari tabel statistik deskriptif di atas, diperoleh beberapa insight penting mengenai distribusi harga saham TLKM:

- **Jumlah Data Konsisten**  
   Semua fitur harga memiliki jumlah entri yang sama, yaitu 1212 baris data, menandakan tidak ada missing value pada kelima fitur ini.

- **Nilai Rata-Rata (Mean)**  
  Harga penutupan (`Close`) rata-rata berada di sekitar **Rp 3.648**, sedikit lebih tinggi dibanding harga pembukaan (`Open`) rata-rata sebesar **Rp 3.651**.  
   - Hal ini menunjukkan bahwa secara umum, harga saham TLKM cenderung **stabil** atau mengalami kenaikan tipis dalam satu hari perdagangan.

- **Volatilitas (Standar Deviasi)**  
   Nilai `std` yang cukup tinggi (sekitar 500) menunjukkan bahwa **fluktuasi harian cukup besar**, mencerminkan dinamika pasar saham TLKM yang aktif dan berisiko sedang-tinggi.

- **Rentang Harga (Min - Max)**
  Harga terendah (`Low`) menyentuh **Rp 2.450**, sedangkan harga tertinggi (`High`) mencapai **Rp 4.850**, menunjukkan **rentang fluktuasi sekitar 98%** selama periode data.

- **Distribusi Harga (25% - 75%)**  
  Harga `Close` 50% dari data berada di antara **Rp 3.190** (Q1) dan **Rp 4.030** (Q3), dengan nilai tengah (median) di **Rp 3.720**.  
   - Distribusi yang tidak terlalu simetris ini menunjukkan bahwa saham TLKM lebih sering berada dalam kisaran menengah ke atas dari rentang harganya.

-  **Kesesuaian Fitur Harga**  
  Fitur `Open`, `High`, `Low`, dan `Close` memiliki pola distribusi yang sangat mirip, mendukung bahwa data saham ini **konsisten secara struktur** dan siap digunakan dalam analisis time series.
  
2. **EDA - Menangani Missing Value**

| No | Kolom      | Jumlah Nilai Hilang |
|----|------------|----------------------|
| 1  | Date       | 0                    |
| 2  | Adj Close  | 0                    |
| 3  | Close      | 0                    |
| 4  | High       | 0                    |
| 5  | Low        | 0                    |
| 6  | Open       | 0                    |
| 7  | Volume     | 0                    |

3. **EDA - Menangani Outlier**
   
### 🚨 Jumlah Outlier per Kolom (Metode IQR)

| No | Kolom      | Jumlah Outlier |
|----|------------|----------------|
| 1  | Adj Close  | 0              |
| 2  | Close      | 0              |
| 3  | High       | 0              |
| 4  | Low        | 0              |
| 5  | Open       | 0              |
| 6  | Volume     | 64             |

![image](https://github.com/user-attachments/assets/604a170a-78f3-445d-ba06-44c801828f39)

![image](https://github.com/user-attachments/assets/370aa8a2-83f0-4275-80ee-2fa3fd67723f)

![image](https://github.com/user-attachments/assets/7b7d0a6b-e560-4d38-9b74-37139762f486)

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

![image](https://github.com/user-attachments/assets/46b1b068-32ff-4e40-a1ee-639b90bdfd7e)

![image](https://github.com/user-attachments/assets/07757fee-14b7-414a-9935-7b8cf1987f5c)



4. **EDA - Univariate Analysis**

![image](https://github.com/user-attachments/assets/99c549af-08bc-45b9-8c07-cb4ff1f15b8f)

![image](https://github.com/user-attachments/assets/aa0506f2-aa5d-47d7-9a76-3e089cb88d34)

![image](https://github.com/user-attachments/assets/6df65556-0e81-4fe2-9eaf-8c9dc6a9c7e0)


5. **EDA - Multivariate Analysis**

![image](https://github.com/user-attachments/assets/4752d126-fae3-4837-ac31-b814c78bcd47)

![image](https://github.com/user-attachments/assets/21002587-cf79-4a04-8dc5-04f78ffea7e0)



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

📌 **Catatan:**

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**


