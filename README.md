# Car_Purchased_Decision
# Laporan Proyek Machine Learning - Felix Pratamasan

## Domain Proyek

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Pada zaman sekarang pembelian suatu barang sangatlah tinggi, setiap harinya banyak *customers* yang melakukan keputusan untuk membeli produk atau tidak[2]. *E-commerce* maupun penjualan barang-barang mewah seperti mobil, motor, perhiasan, dan lain-lain sangat mudah ditemui. 
Dengan adanya teknologi, setiap manusia dapat melihat penjualan-penjualan tersebut. Tidak hanya itu dengan adanya teknologi juga dapat menguntungkan para penjual
dikarenakan penjualan dapat dengan mudah dilakukan dengan *gadget*. Para pengusaha yang melakukan penjualan pun perlu mengetahui pembeli mereka apakah mereka akan membeli
barang tersebut atau tidak. Dengan mengetahui pembeli-pembeli mereka, pengusaha akan dengan mudah untuk menentukkan target market mereka dan tentu saja ini akan menambah
penghasilan dari suatu perusahaan. Sebagai salah satu faktor yang mempengaruhi perilaku pembelian konsumen, gaya *decision-making* sangat penting untuk
memahami perilaku belanja konsumen dan untuk mengembangkan strategi pemasaran yang sukses[1].

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Oleh karena itu, dengan adanya *machine learning* dapat membantu pengusaha untuk mengenali lebih dalam target market mereka dan menambah penghasilan suatu perusahaan.
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

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Data yang digunakan meruapakn data penjualan mobil yang diambil dari kaggle Dataset memiliki jumlah baris yaitu 1000 baris dan 5 kolom. Isi dari dataset ini adalah detail mengenai 1000 customers yang memiliki kecenderungan untuk membeli mobil, berdasarkan dari penghasilan tahunan mereka.

[Cars= Purchased Decision Dataset](https://www.kaggle.com/datasets/gabrielsantello/cars-purchase-decision-dataset) 

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- Users ID : merupakan id customers untuk membedakan tiap customers.
- Age : merupakan usia dari tiap customers.
- AnnualSalaries: merupakan penghasilan tahunan dari tiap customers.
- Purchased: merupakan target kolom sebagai penentu apakah customer akan membeli mobil (1) atau tidak (0) 

**Rubrik/Kriteria Tambahan (Opsional)**:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Pada project ini dilakukan exploratory pada dataset untuk mengetahui informasi dataset lebih lanjut, adapun tahapan exploratory dataset sebagai berikut:

- data.info(): untuk melihat informasi semua features yang ada di dataset. Pada tahap ini informasi yang diberikan adalah berupa informasi umum yang ada di dataset, seperti *range index* yaitu dari 0 - 999, jumlah baris yaitu 1000, jumlah kolom yaitu 5 (*User ID, Gender, Age, AnnualSalary, Purchased*), *datatypes* yaitu 4 kolom *dtype*-nya adalah int64, dan 1 kolom *dtype*-nya adalah *object*
- data.describe(): untuk melihat informasi semua features secara statistik seperti mean tiap kolom, dll.
- data.isnull().sum(): untuk melihat jumlah missing value yang ada pada tiap features
- plot heatmap correlation: untuk melihat korelasi antar kolom pada dataset
- data['Purchased'].value_counts(): untuk melihat berapa banyak jumlah customers yang membeli dan yang tidak membeli
- max() dan min() pada age dan annual salaries: untuk melihat berapa usia tertinggi dan terendah, dan penghasilan tertinggi dan terendah.
- histogram plot: untuk memvisualisasikan features
- box plot: untuk memvisualisasikan features guna mencari outliers

## Data Preparation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Data preparation yang dilakukan pada project ini adalah dengan menggunakan one hot encoding untuk mengubah data categorical menjadi data numerical. Melakukan standarisasi data dan melakukan train test split data 

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Pada data preparation yang pertama dilakukan adalah dengan membuat variabel x (independent) dan variable y (dependent)
- melakukan nomralisasi dengan StandardScaler() terhadap data X dikarenakan data X memiliki nilai yang tidak seimbang dalam skala oleh karena itu diperlukan normalisasi agar skala dari nilainya yaitu 0-1
- Melakukan train test split data agar dapat membedakan data train yang akan digunakan untuk training model dan data testing yang digunakan untuk menguji model dengan data baru.

## Modeling

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Untuk modeling, algoritma yang digunakan adalah Random Forest Classifier dikarenakan algoritma ini merupakan salah satu algoritma supervised learning dan termasuk dalam kasus klasifikasi. Parameter yang digunakan untuk model ini adalah n_estimators = 400 dan citerion = gini. parameter ini digunakan karena hasil parameter terbaik berdasarkan grid seacrh

## Evaluation
Pada tahap evaluasi, project ini menggunakan:
- mean squared error: 12%
- accuracy score: 87%
- confussion matrix: (tp: 114, tn: 12, fp: 13, fn: 61)
- Classification report: 
      
      - (precision 0: 90%, precision 1: 84%)
      - (recall 0:  90%, recall: 82%)
      - (f1 score 0: 90%, f1 score 1: 83%)

## Conclusion

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Decision-making* yang dilakukan untuk melakukan pembelian atau tidak terhadap suatu produk sering dialami oleh *customer* tentunya tidak semua *customer* dapat membeli atau memiliki keinginan untuk membeli produk tersebut. Hal itu dapat membuat perusahan kesulitan untuk mengerti calon pembeli yang pas untuk produknya. Akan tetapi dengan adanya *machine learning* hal itu dapat diatasi, dengan menggunakan algoritma *Random Forest Classsifier* untuk mengklasifikasi *customer* yang ingin membeli dan yang tidak membeli. Dengan itu perusahaan dapat mengerti tipikal pembeli yang sesuai dengan produk dan meningkatkan pemasaran dan mengerti *target* pasar yang ingin dicapai. Studi kasus ini mengangkat persoalan *desicion-making* pada penjualan mobil, dengan menggunakan algoritma *machine learning*, kita bisa tahu mana saja pembeli yang akan melakukan pembelian mobil, untuk akurasi dari modelnya sendiri ialah 87% dan *mean squared error* hanya 12%

## References
[1]Hamedani, Seyed E.A.H, *"A Review of Consumer Decision-Making Styles: Existing Styles and Proposed Additional Styles"* vol.7, 2017.

[2]Stubeid, Saavi, and Arandjelovic, Ognjen, *"Machine Learning Based Prediction of Consumer Purchasing Decisions: The Evidence and Its Significance"* 2018.

## Lampiran

**Korelasi Fitur**

![image](https://user-images.githubusercontent.com/91602612/183862246-dbe96bc7-2d09-42e5-8dd0-83ff76153c3a.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Gambar di atas merupakan plot menggunakan *heat map* untuk melihat korelasi dari tiap fitur yang ada di dataset. pada *matrix correlation* di atas bisa dilihat bahwa fitur *User ID* dan *Gender* memiliki korelasi yang sangat rendah terhadap tiap fitur yang ada di dataset dan memiliki korelasi yang rendah juga terhadap kolom *target / label (purchases)*, oleh karena itu kita perlu untuk menghilangkan kedua fitur tersebut agar akurasi yang akan dihasilkan nantinya menjadi lebih baik. 

**

