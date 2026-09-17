## Analisis Numerik : Regresi & Pencarian Akar pada Studi Kasus BEP Gerai Donat

**Nama :** Sandi Fadia Aizena 

**NPM :** 25083010009 

**Mata Kuliah :** Analisis Numerik


## **Deskripsi Tugas**

Tugas ini menganalisis data laba/rugi harian dari lima gerai donat dengan strategi marketing yang berbeda, menggunakan dua metode numerik utama:

1. Regresi — untuk menemukan bentuk hubungan antara volume penjualan dan revenue.

2. Pencarian Akar (Root Finding) — untuk menentukan titik Break Even Point (BEP) / titik impas dari masing-masing gerai.

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
