# Car_Purchased_Decision
# Laporan Proyek Machine Learning - Felix Pratamasan

## Domain Proyek

Pada zaman sekarang pembelian suatu barang sangatlah tinggi, E-commerce maupun penjualan barang-barang mewah seperti mobil, motor, perhiasan, dan lain-lain sangat mudah ditemui. 
Dengan adanya teknologi, setiap manusia dapat melihat penjualan-penjualan tersebut. Tidak hanya itu dengan adanya teknologi juga dapat menguntungkan para penjual
dikarenakan penjualan dapat dengan mudah dilakukan dengan gadget. Para pengusaha yang melakukan penjualan pun perlu mengetahui pembeli mereka apakah mereka akan membeli
barang tersebut atau tidak. Dengan mengetahui pembeli-pembeli mereka, pengusaha akan dengan mudah untuk menentukkan target market mereka dan tentu saja ini akan menambah
penghasilan dari suatu perusahaan. Oleh karena itu, dengan adanya machine learning dapat membantu pengusaha untuk mengenali lebih dalam target market mereka dan menambah penghasilan suatu perusahaan.
Pada studi kasus ini, contoh pengenalan pembeli yang diambil adalah penjualan mobil untuk menentukkan keputusan penjualan terhadapa calon pembeli.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Masalah ini perlu diselesaikan karena jika tidak maka pengusaha kesulitan untuk mengetahui target market mereka dan akhirnya hanya akan membuang uang untuk melakukan promosi ke target market yang salah
- [A Review of Consumer Decision-Making Styles: Existing Styles and Proposed Additional Styles](https://www.researchgate.net/publication/351251984_A_Review_of_Consumer_Decision-Making_Styles_Existing_Styles_and_Proposed_Additional_Styles)
- [Machine Learning Based Prediction of Consumer Purchasing Decisions: The Evidence and Its Significance](https://core.ac.uk/download/pdf/158368656.pdf)

## Business Understanding

Bagian laporan ini mencakup:

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
- Kurangnya pemahaman penjual terhadap calon pembeli
- Kurangnya pemahaman pasar penjualan

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- Menganalisis data pelanggan sebagai referensi untuk calon pembeli apakah calon pembeli akan membeli atau tidak
- Menggunakan machine learning untuk membantu memahami pasar dengan desicion making analysis dari data pelanggan

Semua poin di atas harus diuraikan dengan jelas. Anda bebas menuliskan berapa pernyataan masalah dan juga goals yang diinginkan.

## Data Understanding

Data yang digunakan meruapakn data penjualan mobil yang diambil dari kaggle [Cars= Purchased Decision Dataset](https://www.kaggle.com/datasets/gabrielsantello/cars-purchase-decision-dataset)
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

