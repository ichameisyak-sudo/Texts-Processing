# Text Data Extraction, Preprocessing, & Sentiment Analysis Pipeline

Repositori ini berisi notebook Python untuk melakukan pengolahan data berbasis teks menggunakan kombinasi teknik ekstraksi data (**Web Scraping via HTTP** & **API Fetching**), **Text Preprocessing**, **Sentiment Analysis**, **Topic Modeling**, hingga visualisasi data.

---

## Deskripsi Proyek

Proyek ini berfokus pada alur pemrosesan data teks secara menyeluruh, mulai dari tahap pengambilan data hingga analisis tingkat lanjut:

- **Ekstraksi Data:** Mengambil artikel berita dari Detik.com menggunakan `requests` dan `BeautifulSoup`, serta menarik data JSON publik secara otomatis melalui REST API (Spaceflight News API).
- **Pembersihan Data (Text Cleaning):** Menghapus elemen non-isi seperti iklan (*SCROLL TO CONTINUE WITH CONTENT*), video, header lokasi (*Jakarta -*), serta tautan internal (*Baca juga*, *[Gambas:]*).
- **Preprocessing & Pemodelan NLP:** Melakukan pembersihan teks bahasa Indonesia melalui *case folding*, tokenisasi, *stopword removal*, dan *stemming* (`Sastrawi`), dilanjutkan dengan pembobotan TF-IDF untuk pemodelan analisis sentimen.
- **Unsupervised Clustering & Validation:** Mengelompokkan teks menggunakan algoritma K-Means berdasarkan matriks TF-IDF, mengevaluasi cluster dengan *Elbow Method* dan *Silhouette Score*.
- **Topic Modeling & Evaluation:** Mengidentifikasi topik-topik tersembunyi pada teks ringkasan berita menggunakan algoritma *Latent Dirichlet Allocation* (LDA) via Gensim, diukur menggunakan *Coherence Score*, serta divisualisasikan secara interaktif.
- **Visualisasi:** Menampilkan hasil ekstraksi data ke dalam bentuk `pandas.DataFrame`, visualisasi kata kunci menggunakan grafik *WordCloud*, serta peta topik interaktif menggunakan `pyLDAvis`.

---

## Library yang Digunakan

- `requests` — Mengirim HTTP Request ke server/API.
- `beautifulsoup4` — Melakukan parsing struktur HTML.
- `pandas` — Menyusun dan menampilkan data dalam bentuk tabular (DataFrame).
- `re` — *Regular Expression* untuk cleaning teks dari pola iklan/noise.
- `nltk` — Pemrosesan bahasa alami (stopwords & tokenisasi).
- `Sastrawi` — Library khusus untuk stemming teks bahasa Indonesia.
- `gensim` — Ekstraksi model LDA (*Latent Dirichlet Allocation*) dan pengukuran *Coherence Score*.
- `pyLDAvis` — Visualisasi interaktif hasil ekstraksi topik LDA.
- `scikit-learn` — Ekstraksi fitur TF-IDF, pemodelan K-Means clustering, dan klasifikasi Random Forest.
- `wordcloud` — Membuat visualisasi awan kata dari frekuensi teks tiap cluster.
- `matplotlib` — Menampilkan grafik visualisasi WordCloud, Elbow Curve, dan hasil analisis.

---

## Cara Menjalankan

1. Clone repositori ini:
   ```bash
   git clone [https://github.com/ichameisyak-sudo/Texts-Processing.git](https://github.com/ichameisyak-sudo/Texts-Processing.git)
