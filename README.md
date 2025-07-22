# Rekomendasi film menggunakan metode Doument Similarity
## Menggunakan dataset yang bersumber pada : 
https://www.kaggle.com/datasets/muqarrishzaib/tmdb-10000-movies-dataset

## Netflix Film Recommended System
Sistem ini membangun sebuah sistem rekomendasi film berbasis similarity/kesamaan dokumen (content-based) menggunakan data film dari TMDB (The Movie Database) dan Natural Language Processing (NLP). Sistem ini dapat merekomendasikan film yang mirip berdasarkan deskripsi/overview film.

### Fitur Utama
Pra-pemrosesan Teks: Membersihkan dan menormalisasi overview film.
Ekstraksi Fitur: Menggunakan TF-IDF untuk mengubah teks menjadi representasi numerik.
Penghitungan Similarity: Menghitung kemiripan antar film dengan Cosine Similarity.
Rekomendasi Film: Menemukan film paling mirip berdasarkan overview.
Alur Notebook

Dataset: TMDB 10000 Movies Dataset.csv
Kolom utama: title, overview, popularity
Data diurutkan berdasarkan popularitas.
Pra-pemrosesan Data

Menghilangkan baris dengan overview kosong.
Menormalisasi teks: lowercasing, menghapus karakter spesial, menghilangkan stopwords, memperbaiki kontraksi.
Ekstraksi Fitur (TF-IDF)

Menggunakan TfidfVectorizer (unigram & bigram, min_df=2) untuk menghasilkan matriks representasi dokumen.
Penghitungan Kemiripan Dokumen

Menggunakan cosine similarity untuk mendapatkan tingkat kemiripan antar film.
Fungsi Rekomendasi

Notebook menyusun pipeline yang bisa digunakan untuk membangun fungsi rekomendasi film berbasis similarity dokumen.
