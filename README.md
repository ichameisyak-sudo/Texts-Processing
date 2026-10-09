# Text Data Extraction, Preprocessing, & Sentiment Analysis Pipeline

Repositori ini berisi notebook Python untuk melakukan pengolahan data berbasis teks menggunakan kombinasi teknik ekstraksi data (**Web Scraping via HTTP** & **API Fetching**), **Text Preprocessing**, **Sentiment Analysis**, hingga visualisasi data.

---

## Deskripsi Proyek

Proyek ini berfokus pada alur pemrosesan data teks secara menyeluruh, mulai dari tahap pengambilan data hingga analisis tingkat lanjut:

- **Ekstraksi Data:** Mengambil artikel berita dari Detik.com menggunakan `requests` dan `BeautifulSoup`, serta menarik data JSON publik secara otomatis melalui REST API (Spaceflight News API).
- **Pembersihan Data (Text Cleaning):** Menghapus elemen non-isi seperti iklan (*SCROLL TO CONTINUE WITH CONTENT*), video, header lokasi (*Jakarta -*), serta tautan internal (*Baca juga*, *[Gambas:]*).
- **Preprocessing & Pemodelan NLP:** Melakukan pembersihan teks bahasa Indonesia melalui *case folding*, tokenisasi, *stopword removal*, dan *stemming* (`Sastrawi`), dilanjutkan dengan pembobotan TF-IDF untuk pemodelan analisis sentimen.
- **Visualisasi:** Menampilkan hasil ekstraksi data ke dalam bentuk `pandas.DataFrame` serta visualisasi kata kunci menggunakan grafik *WordCloud*.

---

## Library yang Digunakan

- `requests` — Mengirim HTTP Request ke server/API.
- `beautifulsoup4` — Melakukan parsing struktur HTML.
- `pandas` — Menyusun dan menampilkan data dalam bentuk tabular (DataFrame).
- `re` — *Regular Expression* untuk cleaning teks dari pola iklan/noise.
- `nltk` — Pemrosesan bahasa alami (stopwords & tokenisasi).
- `Sastrawi` — Library khusus untuk stemming teks bahasa Indonesia.
- `scikit-learn` — Ekstraksi fitur TF-IDF dan pemodelan klasifikasi sentimen.
- `wordcloud` — Membuat visualisasi awan kata dari frekuensi teks.
- `matplotlib` — Menampilkan grafik visualisasi WordCloud dan hasil analisis.

---

## Cara Menjalankan

1. Clone repositori ini:
   ```bash
   git clone [https://github.com/ichameisyak-sudo/Web-Scraping.git](https://github.com/ichameisyak-sudo/Web-Scraping.git)
