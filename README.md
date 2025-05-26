# Analisis Clustering Produk Farmasi di Sumatera Menggunakan Ekosistem Hadoop
## Deskripsi Produk 
Proyek ini bertujuan untuk melakukan analisis clustering terhadap data produk farmasi di Wilayah Sumatera menggunakan Algoritma **K-Means** dalam **Ekosistem Hadoop** .
## Tujuan
Proyek ini bertujuan untuk membantu perusahan farmasi dalam mengelompokkan produk berdasarkan kategori wilayah, kateogri obat , dan informasi lainnya yang relevan sehingga pengelolaan ketersediaan obat yang lebih optimal dan tepa sasaran
## Dataset
Data yang digunakan merupakan data transaksi farmasi tahun **2020-2023** yang mencakup informasi produk, pelanggan, kategori, diskon, rating dan lokasi cabang

## Arsitektur Sistem 
Sistem dibangun berdasaran **Medalion Architectur**, yang membagi prpses pipeline menjaid tiga lapisan:
- **Bronze Layer**: Data mentah dari berbagai sumber.
- **Silver Layer**: Data hasil pembersihan, transformasi, dan integrasi.
- **Gold Layer**: Data siap pakai untuk analisis dan visualisasi.

