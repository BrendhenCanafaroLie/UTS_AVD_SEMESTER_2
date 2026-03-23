# UTS_AVD_SEMESTER_2
# 📊 Exploratory Data Analysis — Netflix Titles Dataset

 Tugas Perorang — Mata Kuliah **Analitik Data dan Visualisasi**
 
 Nama     : Brendhen Canafaro Lie
 
 NIM      : 2509116033
 
 Kelas    : A
 
 Angkatan : 2025
 
---

## Latar Belakang

Netflix adalah platform streaming terbesar di dunia dengan lebih dari 200 juta pelanggan aktif. Dataset **Netflix Titles** merupakan data publik yang berisi informasi lengkap mengenai konten yang tersedia di Netflix hingga tahun 2021 — mencakup **8.807 judul** dengan **12 atribut** seperti tipe konten, genre, negara produksi, tahun rilis, rating, dan durasi.

Analisis ini bertujuan untuk **memahami pola dan karakteristik konten Netflix** melalui pendekatan Exploratory Data Analysis (EDA).

---

## Tujuan Analisis (Analytic Goals)

1. **Comparison** — Genre dan tipe konten apa yang paling dominan di Netflix?
2. **Composition** — Negara mana yang paling banyak memproduksi konten Netflix?
3. **Distribution** — Bagaimana distribusi dan tren konten Netflix dari waktu ke waktu?
4. **Relationship** — Bagaimana hubungan antara rating konten dengan tipe dan genre?

---

## Struktur Repository

```
📦 EDA-Netflix-Titles
 ┣ 📂 Dataset_Film                   ← Notebook utama (EDA lengkap)
 ┣ 📓 EDA                            ← Notebook berisi EDA
 ┣ 📓 Laporan_PDF                    ← Laporan PDF
 ┣ 📓 Latar_Belakang                 ← Notebook berisi Latar Belakang
 ┣ 📓 Tahapan_Proses                            ← Notebook berisi Tahapan Proses
 ┣ 📄 README.md                      ← Dokumentasi proyek

```

---

## Dataset

- **Nama:** Netflix Movies and TV Shows
- **Sumber:** [Kaggle — shivamb/netflix-shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Jumlah Data:** 8.807 baris × 12 kolom
- **Format:** CSV (sudah melalui tahap preprocessing/cleaning)

### Deskripsi Kolom

| Kolom | Tipe | Deskripsi |
|---|---|---|
| `show_id` | object | ID unik setiap konten |
| `type` | object | Jenis konten: Movie atau TV Show |
| `title` | object | Judul konten |
| `director` | object | Nama sutradara |
| `cast` | object | Daftar nama pemain |
| `country` | object | Negara produksi |
| `date_added` | object | Tanggal konten ditambahkan ke Netflix |
| `release_year` | int64 | Tahun rilis konten |
| `rating` | object | Rating usia penonton (TV-MA, PG-13, dll) |
| `duration` | object | Durasi film (menit) atau series (season) |
| `listed_in` | object | Genre konten |
| `description` | object | Sinopsis singkat |

---

## Tahapan Analisis

### 1. Import Library
Menggunakan `pandas`, `numpy`, `matplotlib`, dan `seaborn`.

### 2. Memuat Dataset
Load file CSV, konversi kolom `date_added` ke datetime, ekstraksi fitur `year_added`, `month_added`, dan `primary_country`.

### 3. Exploratory Data Analysis (EDA)
Terdapat **8 visualisasi terpisah**, masing-masing dilengkapi insight dan rekomendasi tindakan.

---

## Hasil EDA

### Comparison

<img width="680" height="480" alt="image" src="https://github.com/user-attachments/assets/fe319e6b-58b8-435a-bb7b-7883e8a7e30d" />

**1.1 Movie vs TV Show**
- Movie mendominasi dengan **6.131 judul (69.6%)** vs TV Show 2.676 judul (30.4%)
- Rasio hampir 7:3 — dari setiap 10 konten, 7 di antaranya film
- **Rekomendasi:** Netflix perlu menambah porsi TV Show untuk meningkatkan retensi pengguna karena series cenderung membuat penonton kembali

<img width="880" height="580" alt="image" src="https://github.com/user-attachments/assets/40e64d69-42f0-48e3-8dbe-79ece731d039" />
**1.2 Top 10 Genre Terpopuler**
- International Movies (2.752), Dramas (2.427), Comedies (1.674) mendominasi
- Netflix aktif menghadirkan konten dari berbagai negara dan budaya
- **Rekomendasi:** Kreator konten Indonesia berpeluang besar masuk Netflix lewat genre International Movies

---

### Composition

<img width="779" height="691" alt="image" src="https://github.com/user-attachments/assets/ee92889c-e7f0-45d5-84fc-4c0438de5486" />

**1.3 Proporsi Negara Produksi (Pie Chart)**
- United States mendominasi ~40% dari seluruh konten
- Kategori Others (~28%) menunjukkan potensi besar dari negara-negara yang belum terwakili
- **Rekomendasi:** Strategi konten lokal perlu diperkuat untuk menjangkau pengguna di negara berkembang

<img width="980" height="480" alt="image" src="https://github.com/user-attachments/assets/99183245-3673-4f92-ae78-6b3dd85ad8ea" />

**1.4 Top 10 Negara Produksi (Bar Chart)**
- United States (2.818) memimpin jauh, hampir 3x lipat India (972) di posisi kedua
- South Korea (199) masuk top 5 meski negara kecil — didorong popularitas K-Drama global
- **Rekomendasi:** Keberhasilan Korea bisa menjadi model — konten berkualitas bisa melampaui keterbatasan ukuran negara

---

### Distribution

<img width="980" height="480" alt="image" src="https://github.com/user-attachments/assets/fbd3de7c-1dde-4536-b514-4cd784c9c890" />

**1.5 Distribusi Tahun Rilis (Histogram)**
- Distribusi right-skewed — mayoritas konten dari tahun 2015–2021
- Median tahun rilis: **2017**
- **Rekomendasi:** Netflix perlu menambah koleksi film klasik sebagai daya tarik segmen penonton yang lebih tua

<img width="1080" height="480" alt="image" src="https://github.com/user-attachments/assets/c4255d63-a44e-48f0-be1c-c7876bacec0f" />

**1.6 Tren Penambahan Konten per Tahun (Line Chart)**
- Pertumbuhan pesat dari 2015 (756) hingga puncak **2019 (1.497 konten)**
- Penurunan di 2020–2021 akibat dampak pandemi COVID-19
- **Rekomendasi:** Investasi di Netflix Original bisa jadi solusi agar tidak bergantung pada studio eksternal

---

### Relationship

<img width="1080" height="480" alt="image" src="https://github.com/user-attachments/assets/7586bc22-67db-4fd8-9dec-6279f33ec652" />

**1.7 Rating berdasarkan Tipe Konten (Grouped Bar)**
- TV-MA adalah rating paling dominan, terutama dari TV Show
- Movie lebih banyak menggunakan rating R dan PG-13, TV Show mayoritas TV-MA dan TV-14
- **Rekomendasi:** Netflix perlu memperbanyak konten kids untuk bersaing dengan Disney+ di segmen anak-anak

<img width="942" height="480" alt="image" src="https://github.com/user-attachments/assets/455ae7fb-d00c-4b56-b425-49c32e75d3da" />

**1.8 Heatmap Genre vs Rating**
- Dramas + TV-MA adalah kombinasi paling dominan di seluruh katalog
- Comedies lebih merata di semua rating — genre paling inklusif untuk semua usia
- **Rekomendasi:** Kreator yang ingin masuk Netflix sebaiknya membuat Drama dengan rating TV-MA karena ini kombinasi paling diminati platform

---

## Kesimpulan

**Comparison:** Movie mendominasi (69.6%), genre terbanyak International Movies — Netflix aktif ekspansi konten global.

**Composition:** United States produsen terbesar (~36%), diikuti India (~12%). Katalog masih sangat US-sentris meski mulai beragam.

**Distribution:** Mayoritas konten dari era 2015–2021 (median: 2017). Puncak penambahan di 2019, turun akibat pandemi.

**Relationship:** Netflix jelas menyasar penonton dewasa — TV-MA paling dominan. Drama dewasa menjadi konten andalan, Comedy paling inklusif.

---

## Library yang Digunakan

```python
pandas
numpy
matplotlib
seaborn
```

---

## Cara Menjalankan

1. Clone repository ini
```bash
git clone https://github.com/username/EDA-Netflix-Titles.git
cd EDA-Netflix-Titles
```

2. Upload file `netflix_titles(Bersih).csv` ke Google Colab

3. Buka notebook `EDA_Netflix_Fixed.ipynb` di Google Colab

4. Pastikan path dataset sesuai
```python
file = "/content/netflix_titles(Bersih).csv"
```

5. Klik **Runtime → Run all** 

