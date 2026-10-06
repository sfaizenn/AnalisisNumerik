# Analisis Numerik : Integrasi Numerik pada Studi Kasus Volume Lambung Perahu Katamaran

**Nama :** Sandi Fadia Aizena

**NPM :** 25083010009

**Mata Kuliah :** Analisis Numerik


### **Deskripsi Tugas**
Tugas ini menghitung volume kedua lambung perahu katamaran fiberglass untuk wisata pancing berdasarkan gambar tampak atas dan tampak samping yang diberi grid. Pada revisi ini, skala grid diperbaiki menjadi satu kotak grid = 45 cm.

Metode yang digunakan yaitu:
1. **Pengukuran dimensi dari gambar** untuk memperoleh lebar lambung (tampak atas) dan tinggi lambung (tampak samping) pada setiap jarak 1 kotak (45 cm).
2. **Integrasi numerik (aturan trapesium dan aturan Simpson 1/3)** untuk menjumlahkan luas penampang sepanjang lambung menjadi volume.

### **Tujuan**
1. Menentukan lebar dan tinggi lambung dari gambar bergrid dengan skala satu kotak grid = 45 cm.
2. Menghitung luas penampang lambung pada setiap titik memanjang, dengan anggapan lantai kapal datar (tanpa keel) sehingga tampak depan berbentuk persegi panjang.
3. Menerapkan integrasi numerik (aturan trapesium dan Simpson 1/3) untuk menghitung volume satu lambung, tanpa memasukkan volume reserve buoyancy.
4. Menghitung volume kedua lambung dan mengimplementasikan seluruh proses menggunakan Python.

### **Objek yang Dianalisis**
| Bagian | Keterangan |
|--------|------------|
| Lambung atas dan bawah (tampak atas) | Identik, sehingga V_total = 2 × V_satu lambung |
| Reserve buoyancy | Ujung buritan dan ujung haluan, tidak dihitung |
| Bagian yang dihitung | Antara batas reserve buoyancy kiri dan kanan (x = 2 sampai 18 kotak, atau x = 90 sampai 810 cm) |

### Data dan Ketentuan
Gambar yang digunakan adalah perahu.pdf yang memuat tampak atas dan tampak samping perahu katamaran.

Sumber gambar:
https://www.researchgate.net/publication/342077926_Desain_dan_Konstruksi_Perahu_Katamaran_Fiberglass_untuk_Wisata_Pancing

Ketentuan soal:
- Satu kotak grid = 45 cm (satu dash-kosong = 5 + 5 cm).
- Lantai kapal dianggap datar (tanpa keel), sehingga tampak depan semuanya persegi panjang.
- Volume reserve buoyancy tidak dihitung.

Variabel yang digunakan dalam analisis antara lain:
- `x` : posisi memanjang lambung (kotak dan cm)
- `w` : lebar lambung dari tampak atas (kotak dan cm)
- `d` : tinggi lambung dari tampak samping (kotak dan cm)
- `A = w × d` : luas penampang (cm²)

### Metodologi
1. **Kalibrasi Skala**
   Garis grid hijau pada gambar dideteksi secara otomatis (21 garis vertikal dan 17 garis horizontal, sekitar 51,50 piksel per kotak). Satu kotak grid ditetapkan sebesar 45 cm, sehingga lebar grid 20 kotak setara 900 cm.
2. **Pengukuran Dimensi**
   Lebar `w` diukur dari tampak atas dan tinggi `d` diukur dari tampak samping (garis geladak sampai dasar datar) pada x = 2, 3, ..., 18 kotak (17 titik data). Hasil pembacaan diverifikasi dengan overlay di atas gambar desain.
3. **Luas Penampang**
   Karena tampak depan berbentuk persegi panjang, luas penampang pada setiap titik adalah `A = w × d`.
4. **Batas Integrasi**
   Reserve buoyancy (di luar x = 2 sampai 18 kotak) tidak dihitung, sehingga integrasi hanya dilakukan pada x = 90 sampai 810 cm (n = 16 interval, h = 45 cm).
5. **Integrasi Numerik**
   Volume satu lambung dihitung dengan dua metode:
   dengan h = 45 cm dan n = 16.

### Hasil
| Metode | Volume 1 lambung | Volume 2 lambung |
|--------|------------------|------------------|
| Aturan trapesium | 6,635 m³ | 13,270 m³ |
| Aturan Simpson 1/3 | 6,646 m³ | 13,292 m³ |

Selisih antara kedua metode sebesar 0,16%.

### Library yang Digunakan
1. `PyMuPDF (fitz)` untuk membaca berkas PDF dan mengonversinya menjadi gambar
2. `numpy` untuk operasi numerik dan array
3. `pandas` untuk menyusun tabel data pengukuran dan tabel hasil
4. `scipy` (fungsi `simpson`) untuk integrasi aturan Simpson 1/3
5. `matplotlib` untuk visualisasi gambar, overlay, dan profil lambung

### Cara Menjalankan
1. Clone atau download repository ini.
2. Buka notebook menggunakan Google Colab.
3. Jalankan setiap cell secara berurutan.
4. Saat diminta pada cell pertama, unggah berkas `perahu.pdf`.
