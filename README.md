# 🏎️ Analisis Data Penjualan BMW Global (2018–2025)

Proyek ini adalah sebuah analisis data / eksplorasi data (EDA) komprehensif terhadap penjualan otomotif global BMW dari tahun 2018 hingga 2025. Proses pengolahan data dan visualisasi disajikan secara interaktif menggunakan Jupyter Notebook. 

## 📂 Struktur Proyek

```text
program/
│
├── dataset/
│   └── bmw_global_sales_2018_2025.csv   # Dataset asli penjualan global BMW
│
├── src/
│   └── train/
│       └── data_train.ipynb             # Notebook utama untuk pengolahan & visualisasi data
│
├── requirements.txt                     # Daftar pustaka Python yang dibutuhkan
└── README.md                            # Dokumentasi utama proyek
```

## 🛠️ Alur Kerja & Fitur Utama

Notebook `src/train/data_train.ipynb` mencakup berbagai fase dalam alur data science:

1. **Load Dataset**: Memuat data mentah penjualan (`bmw_global_sales_2018_2025.csv`).
2. **Pratinjau Data (Preview)**: Pemeriksaan dimensi data, nama kolom, jenis data, serta cuplikan data teratas.
3. **Pembersihan Data (Data Cleaning)**:
   - Evaluasi kelengkapan data (Missing Values) pada `Units_Sold` dan `Region`.
   - Mengatasi nilai kosong (imputasi/drop).
   - Identifikasi dan penghapusan duplikasi data.
4. **Pra-pemrosesan Data (Data Preprocessing)**:
   - Standarisasi konsistensi format teks (misal: pengubahan penulisan bulan "Jan" menjadi angka "1").
   - Transforamasi tipe data untuk kolom berbasis penanggalan, menciptakan index *Datetime* berurutan agar analisis Time-Series menjadi lebih akurat.
5. **Eksplorasi Analisis Data (EDA) & Agregasi**:
   - Menghitung agregat penjualan bulanan global di semua perwakilan / model dengan metode `groupby`.
6. **Visualisasi Time-Series**:
   - Pembuatan grafik *time-series* untuk menemukan tren penjualan bulanan atau tahunan dari tahun 2018 hingga tren prediksi 2025.

## 📦 Persyaratan Library (Requirements)

Seluruh pustaka atau *dependencies* yang diperlukan untuk menjalankan kode ini telah disediakan pada file `requirements.txt`. Library yang akan diunduh meliputi:
- `pandas` (Struktur dan manipulasi tabel)
- `numpy` (Operasi numerik)
- `matplotlib` (Plotting grafik dasar horisontal/vertikal)
- `seaborn` (Keindahan dan penyempurnaan grafik yang dibuat)

## 🚀 Cara Menjalankan Proyek

1. **Clone repository ini** ke komputer Anda.
   ```bash
   git clone https://github.com/muhammadrafifatihulihsan/BMW-Global-Sales-Analysis.git
   cd program
   ```
2. **Instal library (opsional, disarankan dalam Virtual Environment)**:
   ```bash
   pip install -r requirements.txt
   ```
3. Buka Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Navigasikan ke dalam folder `src/train/` dan buka file `data_train.ipynb`. 
5. Jalankan (*Run All*) sel kode (cells) yang ada untuk menduplikasi alur pembersihan dan membuat perbandingan grafik penjualan!

---
> 💡 *Dibuat untuk latihan/praktik pemrosesan dan analisis data menggunakan python. Silakan menjelajah kode dan visualisasinya secara mandiri.*
