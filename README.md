# MUSIC RECOMMENDATION CONTENT BASED FILTERING - QAILA CASANDRA
Proyek ini merupakan proyek ke-dua Machine Learning Terapan, pada proyek ini saya akan memberikan rekomendasi music kepada para user dengan menggunakan model Content Based Filtering

## Domain Proyek
Perkembangan teknologi digital dan penetrasi internet yang masif telah mengubah cara manusia mengakses dan menikmati hiburan, salah satunya adalah musik. Platform layanan streaming seperti Spotify, Apple Music, dan YouTube Music menyediakan jutaan lagu yang dapat diakses kapan saja dan di mana saja oleh penggunanya. Namun, semakin luasnya koleksi musik justru menciptakan tantangan baru: bagaimana membantu pengguna menemukan lagu-lagu yang sesuai dengan preferensi mereka secara efisien dan personal?

Salah satu solusi yang banyak diterapkan dalam mengatasi tantangan tersebut adalah penerapan sistem rekomendasi musik. Sistem ini dirancang untuk memahami pola dan selera pengguna, lalu menyarankan lagu-lagu yang berpotensi disukai. Berbagai pendekatan algoritmik telah digunakan untuk membangun sistem semacam ini, di antaranya adalah collaborative filtering, hybrid systems, dan content-based filtering. Dalam proyek ini, fokus diarahkan pada pendekatan content-based filtering, yaitu metode yang merekomendasikan lagu berdasarkan kesamaan atribut yaitu genre musik. Pendekatan ini memiliki kelebihan karena tidak bergantung pada data pengguna lain (seperti collaborative filtering), sehingga cocok digunakan ketika data interaksi pengguna masih terbatas (cold-start problem).

## Business Understanding
### Problem Statements
adapun rurmusan masalah dari project ini adalah
1. Bagaimana memberikan rekomendasi lagu berdasarkan genre lagu menggunakan machine learning
2. Bagaimana membangun sistem rekomendasi yang efektif dan akurat?
3. Bagaimana mengevaluasi performa model rekomendasi?

### Goals
Berdasarkan rumusan masalah yang telah dirumuskan, berikut merupakan tujuan dari proyek ini
1. Mengimplementasikan *Content-Based Filtering* untuk sistem rekomendasi lagu.
2. Membangun pipeline mulai dari *data wrangling*, *EDA*, hingga *modelling* dan *evaluation*.
3. Memberikan hasil dari model machine learning yang telah dikembangkan

### Solution Statements
Berikut merupakan Solution Statements dari proyek ini
1. Melakukan proses pengembangan model machine learning dari awal yaitu Data Wrangling hingga Evaluation
2. Menggunakan algoritma yang sesuai yaitu content based filtering.
3. Melakukan evaluasi model untyk mengetahui performa model, hal ini dilakukan untuk mengetahui performa dari model yang telah dikembangkandalam memberikan rekomendasi berdasarkan genre.

## Data Understanding
Dataset diperoleh dari Kaggle pada link berikut [Top Hits Spotify from 2000–2019 (Kaggle)](https://www.kaggle.com/datasets/paradisejoy/top-hits-spotify-from-20002019), dari dataset tersebut terdapat 15150 data dengan 18 kolom. Tidak ditemukannya missing value pada dataset ini, namun ditemukan 1 data duplikat. Adapaun kolom pada datset ini adalah sebagai berikut
### Fitur Dataset
1. Track : Judul Lagu
2. Artist : Nama penyanyi dari lagu tersebut
3. Year : Tahun lagu tersebut di rilis
4. Duration : Durasi dari lagu
5. Time_Signature : pola irama dasar dari sebuah lagu
6. Danceability : Seberapa cocok lagu untuk menari (0.0 – 1.0).
7. Energy : Intensitas dan aktivitas lagu (0.0 – 1.0).
8. Key : Tangga nada utama (0–11)
9. Loudness : Tingkat kekerasan suara dalam desibel
10. Mode : Modus skala: 1 = mayor, 0 = minor
11. Speechiness : Kandungan kata-kata dalam lagu (0.0 – 1.0)
12. Acousticness : Kemungkinan bahwa lagu bersifat akustik (0.0 – 1.0)
13. Instrumentalness : Apakah lagu dominan instrumental (nilai tinggi berarti tanpa vokal)
14. Liveness : Keceriaan/kebahagiaan lagu (0.0 = sedih, 1.0 = bahagia)
15. Valence : Keceriaan/kebahagiaan lagu (0.0 = sedih, 1.0 = bahagia)
16. Tempo : Tempo lagu dalam BPM (Beats Per Minute)
17. Popularity :Skor popularitas (biasanya 0–100) berdasarkan platform
18. Genre : Kategori genre lagu (misal: Pop, Rock, Jazz)

## Data Preparation

## Modeling
Pada proyek ini model yang digunakan adalah content based filtering
### Content Based Filtering
![Content-based-music-recommendation-system](https://github.com/user-attachments/assets/dc9b4b3b-0ee5-4a7e-921d-151aaaa29407)
Sistem rekomendasi dengan metode content-based filtering merekomendasikan item yang mirip dengan item sebelumnya yang disukai atau dipilih oleh pengguna. Kemiripan item dihitung berdasarkan pada fitur-fitur yang ada pada item yang dibandingkan. Metode ini bersifat user independence, tidak bergantung pada situasi apakah item tersebut merupakan item baru (yang belum pernah dipilih oleh pengguna manapun) maupun bukan item baru. Jika seorang pengguna telah memesan suatu menu hidangan pada kategori tertentu maka sistem akan mencoba merekomendasikan menu hidangan dengan kategori serupa yang juga tersedia di restoran lain yang mungkin akan disukai juga oleh pengguna tersebut.
Kelemahan : terbatasnya rekomendasi hanya pada item-item yang mirip sehingga tidak ada kesempatan untuk mendapatkan item yang tidak terduga
Kekurangan : Content-based filtering memberikan rekomendasi berdasarkan karakteristik item yang sudah disukai pengguna sebelumnya. Karena fokusnya adalah preferensi individual, sehingga hasil rekomendasi cenderung lebih relevan dan personal
## Evaluation
\text{Precision} = \frac{\text{Jumlah rekomendasi relevan}}{\text{Total rekomendasi}}

## Conclusion
- Sistem rekomendasi lagu berbasis konten berhasil dibangun dan diuji dengan precision 100%.
- Pipeline proyek mencakup *data cleaning*, *feature engineering*, *modeling*, dan *evaluation*.
- Sistem ini relevan untuk digunakan sebagai dasar dalam pengembangan aplikasi musik online.

## Refrensi
Ricci, F., Rokach, L., & Shapira, B. (2015). Recommender Systems Handbook. Springer.
Mondi. (2020). Recommendation system with content‑based filtering method for culinary tourism in Mangan application. ITSmart: Jurnal Teknologi dan Informasi, 9(1)


