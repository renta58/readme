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
## Infrastruktur teknologi
Proyek ini berjalan di lingkungan **Docker** yang berisi komponen-komponen sebagai berikut:

- **HDFS** – Penyimpanan data terdistribusi
- **Apache Spark** – Pemrosesan batch ETL dan analitik
- **Apache Hive** – SQL query engine untuk eksplorasi data
- **Apache Superset** – Visualisasi data interaktif
- **Hive Metastore** – Penyimpanan metadata

Konfigurasi cluster lokal:
- 1 NameNode
- 2 DataNode
- 1 Spark Master
- 2 Spark Worker
  ## Proses Analitik
  Analisis clustering dilakukan dengan **K-Means Clustering** dari pustaka **Apache Spark MLlib**:

1. Membaca data dari Gold Layer (format Parquet)
2. Preprocessing: normalisasi, imputasi missing value
3. Split data ke training dan testing
4. Latih model K-Means
5. Evaluasi performa model
6. Simpan dan deploy model untuk penggunaan lebih lanjut

   ## Implementasi Pipeline
   Pipeline batch dibangun untuk memproses data secara bertahap dari ingest hingga analitik. Proses mencakup:

1. Ingest data ke HDFS
2. Transformasi dan pembersihan dengan Spark
3. Simpan hasil ke Hive
4. Analisis clustering dengan Spark MLlib
5. Visualisasi hasil

## pengujian sistem
Pengujian dilakukan secara menyeluruh:

- **Unit Testing** – Validasi fungsi-fungsi individual (ETL, ingest, transformasi)
- **Integration Testing** – Alur data dari HDFS ke Hive dan Superset
- **Data Quality Testing** – Validasi duplikasi, missing value, dan schema
- **Performance Testing** – Waktu eksekusi pipeline batch
- **End-to-End Testing** – Simulasi jalur penuh dari data mentah ke visualisasi

##  Struktur Folder

```bash
├── data/
│   └── raw/               # Data mentah
├── docker/
│   └── hadoop/            # Konfigurasi Docker Hadoop
├── etl/
│   └── spark_jobs.py      # Script ETL dan preprocessing
├── model/
│   └── kmeans_model.pkl   # Model clustering
├── report/
│   └── visualisasi.png    # Hasil clustering
├── README.md

   
  
