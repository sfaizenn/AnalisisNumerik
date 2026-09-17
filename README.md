## Analisis Numerik : Regresi & Pencarian Akar pada Studi Kasus BEP Gerai Donat

**Nama :** Sandi Fadia Aizena 

**NPM :** 25083010009 

**Mata Kuliah :** Analisis Numerik


## **Deskripsi Tugas**

Tugas ini menganalisis data laba/rugi harian dari lima gerai donat dengan strategi marketing yang berbeda.

Metode yang digunakan yaitu:

1. **Regresi** untuk melihat hubungan antara volume penjualan dan revenue.
2. **Pencarian Akar (Root Finding)** untuk menentukan titik Break Even Point (BEP) atau titik impas dari masing-masing gerai.

## **Tujuan**

1. Menerapkan metode regresi untuk menganalisis dan memodelkan hubungan antara volume penjualan dengan revenue pada lima gerai donat dengan strategi marketing yang berbeda.

2. Membandingkan beberapa bentuk model regresi, yaitu linear, kuadratik, dan eksponensial, untuk menentukan model yang paling sesuai dengan pola data berdasarkan nilai koefisien determinasi (R²).

3. Menerapkan metode numerik pencarian akar (root finding), yaitu metode Bisection, untuk menentukan jumlah volume penjualan yang menghasilkan Break Even Point (BEP) atau titik impas pada masing-masing gerai.

4. Mengimplementasikan konsep regresi dan pencarian akar dalam analisis data penjualan menggunakan Python.

## **Gerai yang Dianalisis**

| Gerai | Strategi Marketing |
|-------|---------------------|
| A     | Premium Gourmet : Harga Tinggi, Niche Terbatas, Kafe Specialty |
| B     | Mass Market Volume : Harga Murah, Margin Tertekan Inflasi Bahan |
| C     | Promo Agresif : Diskon Awal, Iklan Moderate-High |
| D     | Mall Premium Flagship : Sewa Lokasi Tinggi |
| E     | Cloud Kitchen : Fokus App Delivery, Terkena Komisi Platform 18% |

## Dataset

Dataset yang digunakan adalah **sintesis_data_donat_harian.csv** yang berisi data penjualan harian dari lima gerai donat.

Sumber dataset:
https://github.com/jendralhxr/metnummatdis/blob/main/sintesis_data_donat_harian.csv

Variabel yang digunakan dalam analisis antara lain:

- `Gerai`
- `Jumlah Terjual (Unit)`
- `Pendapatan Kotor (Rp)`
- `Biaya Variabel (Rp)`
- `Fixed Cost Harian (Rp)`

## Metodologi

1. Visualisasi Data
Memvisualisasikan hubungan antara jumlah penjualan dan revenue pada kelima gerai menggunakan scatter plot untuk melihat pola hubungan antarvariabel.

2. Regresi
Menerapkan regresi untuk memodelkan hubungan antara volume penjualan dan revenue. Beberapa bentuk model, yaitu linear, kuadratik, dan eksponensial, dibandingkan berdasarkan nilai koefisien determinasi (R²) untuk menentukan model yang sesuai.

3. Pencarian Akar
Menggunakan metode Bisection untuk mencari jumlah volume penjualan saat fungsi profit bernilai nol. Nilai tersebut digunakan untuk menentukan Break Even Point (BEP) pada masing-masing gerai.

4. Analisis Hasil
Menganalisis hasil regresi dan BEP dari masing-masing gerai berdasarkan model yang diperoleh.
- `Gerai`
- `Jumlah Terjual (Unit)`
- `Pendapatan Kotor (Rp)`
- `Biaya Variabel (Rp)`
- `Fixed Cost Harian (Rp)`

## Library yang Digunakan

1. `pandas` untuk pengolahan data
2. `numpy` untuk operasi numerik dan regresi
3. `matplotlib` untuk visualisasi data
4. `scipy.optimize` untuk fitting model eksponensial

## Cara Menjalankan

1. Clone atau download repository ini.
2. Buka notebook menggunakan Google Colab atau Jupyter Notebook.
3. Pastikan dataset tersedia sesuai sumber yang tercantum pada bagian Dataset.
4. Jalankan setiap cell secara berurutan.
