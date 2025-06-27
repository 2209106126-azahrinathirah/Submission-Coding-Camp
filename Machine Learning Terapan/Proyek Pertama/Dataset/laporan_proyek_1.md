# Laporan Proyek Machine Learning - Andi Zahrina Athirah Ahmad

## Domain Proyek
---
**Latar Belakang**
   Prediksi harga saham merupakan tantangan penting dalam dunia keuangan, khususnya di pasar modal Indonesia yang terus berkembang pesat dalam beberapa dekade terakhir. Fluktuasi harga saham yang tinggi disebabkan oleh berbagai faktor seperti kondisi ekonomi makro, kinerja perusahaan, sentimen pelaku pasar, serta situasi geopolitik, menjadikan investasi di pasar saham penuh risiko [1]. Ketidakstabilan ini menyulitkan investor dalam mengambil keputusan yang optimal, terutama untuk jangka menengah dan panjang. Oleh karena itu, dibutuhkan pendekatan prediktif yang mampu mengenali pola-pola kompleks dalam data historis harga saham guna mendukung pengambilan keputusan yang lebih akurat dan berbasis data.[1]
    Salah satu saham yang menarik untuk dianalisis adalah PT Telekomunikasi Indonesia Tbk (TLKM), sebuah perusahaan telekomunikasi milik negara yang termasuk dalam kategori saham blue chip. Saham TLKM aktif diperdagangkan di Bursa Efek Indonesia (BEI) dan memiliki pengaruh besar terhadap indeks utama seperti IHSG dan LQ45[1]. Kemampuan untuk memprediksi harga penutupan saham TLKM secara akurat dapat membantu investor, analis pasar, dan pembuat kebijakan dalam membuat keputusan yang lebih rasional dan berbasis data.
    Model statistik tradisional seperti ARIMA atau regresi linear sering kali tidak mampu menangkap pola nonlinier dan dependensi jangka panjang dalam data time series saham [2]. Untuk menjawab tantangan tersebut, pendekatan berbasis deep learning seperti Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) menjadi solusi yang menjanjikan karena kemampuannya dalam mempelajari urutan data historis dan mengingat informasi jangka panjang. [3]
    Melalui proyek ini, saya mengembangkan dan membandingkan model LSTM dan GRU untuk memprediksi harga penutupan saham TLKM, dengan fokus pada tiga skenario waktu ke depan: 7 hari, 30 hari, dan 60 hari. Evaluasi dilakukan menggunakan metrik MAE, RMSE, dan MAPE untuk menilai sejauh mana model dapat memberikan hasil prediksi yang akurat dan stabil [4].
    
**Rubrik/Kriteria Tambahan (Opsional)**:
**❓ Mengapa Masalah Ini Harus Diselesaikan**
1. Fluktuasi harga saham TLKM yang tinggi membuat investor membutuhkan strategi prediktif berbasis data untuk memaksimalkan return dan meminimalkan risiko.
2. Model statistik konvensional seperti ARIMA atau regresi linear belum mampu menangani data saham yang kompleks, nonlinier, dan bergantung pada urutan waktu.
3. Di era digital, pengambilan keputusan finansial berbasis data dan kecerdasan buatan telah menjadi praktik umum secara global, dan perlu lebih banyak diterapkan di pasar saham Indonesia.

**❓ Bagaimana Masalah Ini Harus Diselesaikan**
1. Mengumpulkan data historis harga saham TLKM dari sumber resmi seperti Yahoo Finance atau Bursa Efek Indonesia.
2. Melakukan preprocessing data time series, termasuk normalisasi dan pembuatan window sekuensial.
3. Membangun dua model deep learning: Long Short-Term Memory (LSTM) dan Gated Recurrent Unit (GRU) untuk mempelajari pola historis.
4. Mengevaluasi performa model menggunakan metrik MAE, RMSE, dan MAPE untuk mengukur akurasi prediksi.
5. Melakukan eksperimen prediksi harga penutupan saham TLKM untuk tiga horizon waktu ke depan:
   - 7 hari (jangka pendek)
   - 30 hari (jangka menengah)
   - 60 hari (jangka panjang)

**Hasil Riset Terkait (Referensi)**
[1] T. Prasetyo and M. Faisal, “Penerapan Data Mining dalam Prediksi Harga Saham di Indonesia Menggunakan Algoritma LSTM,” *Indonesian Journal on Computer and Information Technology (IJCIT)*, vol. 4, no. 2, pp. 116–120, Nov. 2019. doi: 10.31294/ijcit.v4i2.7712.
[2] H. K. Alfredo, “Analysis of Fama and French 3-Factor Model Variables in the Formation of Expected Stock Returns (Issuers of LQ-45 Index Member Stocks for the Period 2020–2022),” *Edunity: Social and Educational Studies*, vol. 2, no. 7, 2023. doi: https://doi.org/10.57096/edunity.v2i7.122
[3] Ridwan, M., Sadik, K., & Afendi, F. (2023). Comparison of ARIMA and GRU Models for High-Frequency Time Series Forecasting. Scientific Journal of Informatics, 10(3), 389–400. doi: https://doi.org/10.15294/sji.v10i3.45965 
[4] Yavasani, R., & Wang, F. (2023). Comparative Analysis of LSTM, GRU, and ARIMA Models for Stock Market Price Prediction. Journal of Student Research, 12(4). https://doi.org/10.47611/jsrhs.v12i4.5888
[5] N. A. Nilsen, "Perbandingan Model RNN, Model LSTM, dan Model GRU dalam Memprediksi Harga Saham-Saham LQ45," Jurnal Statistika dan Aplikasinya, vol. 6, no. 1, pp. 137–147, 2022, doi: https://doi.org/10.21009/JSA.06113



## Business Understanding

Pada bagian ini, kamu perlu menjelaskan proses klarifikasi masalah.

Bagian laporan ini mencakup:

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
- Pernyataan Masalah 1
- Pernyataan Masalah 2
- Pernyataan Masalah n

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- Jawaban pernyataan masalah 1
- Jawaban pernyataan masalah 2
- Jawaban pernyataan masalah n

Semua poin di atas harus diuraikan dengan jelas. Anda bebas menuliskan berapa pernyataan masalah dan juga goals yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Menambahkan bagian “Solution Statement” yang menguraikan cara untuk meraih goals. Bagian ini dibuat dengan ketentuan sebagai berikut: 

    ### Solution statements
    - Mengajukan 2 atau lebih solution statement. Misalnya, menggunakan dua atau lebih algoritma untuk mencapai solusi yang diinginkan atau melakukan improvement pada baseline model dengan hyperparameter tuning.
    - Solusi yang diberikan harus dapat terukur dengan metrik evaluasi.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

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

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

