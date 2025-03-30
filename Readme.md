# Analisis Sentimen Tweet Bencana Alam

Proyek analisis sentimen yang menganalisis tweet terkait bencana alam menggunakan berbagai pendekatan analisis sentimen serta klasifikasi SVM dengan berbagai fungsi kernel.

## Ringkasan

Proyek ini menganalisis data Twitter yang terkait dengan beberapa peristiwa bencana alam:

- Gempa Haiti 
- Gempa Kroasia
- Banjir Catania
- Banjir Eropa

Analisis sentimen dilakukan menggunakan tiga pendekatan berbeda:
- VADER (Valence Aware Dictionary and Sentiment Reasoner)
- TextBlob
- AFINN

Selain analisis individu, proyek ini juga menerapkan **majority voting**, di mana hasil klasifikasi sentimen dari ketiga metode (VADER, TextBlob, dan AFINN) dibandingkan, dan sentimen akhir ditentukan berdasarkan hasil mayoritas dari ketiga pendekatan tersebut. Pendekatan ini membantu meningkatkan akurasi dengan menggabungkan kekuatan masing-masing metode analisis sentimen.

## Fitur

- **Proses Pra-pemrosesan Data:**
  - Pembersihan teks
  - Case folding (penyesuaian huruf besar/kecil)
  - Tokenisasi
  - Penghapusan stopword
  - Stemming
- **Ekstraksi Fitur:** TF-IDF
- **Klasifikasi SVM dengan Berbagai Kernel:**
  - Linear
  - Polinomial
  - RBF (Radial Basis Function)  
  - Sigmoid
- **Metrik Evaluasi Kinerja:**
  - Akurasi
  - Presisi
  - Recall
  - Skor F1
  - Confusion Matrix

## Struktur Proyek

```
sentiment-models/
├── Ground Truth/          # Label sentimen ground truth
├── Hasil Analisis/        # Hasil analisis
├── Kamus Corpus/         # Kamus dan korpus
├── Translate Dataset/     # Dataset yang telah diterjemahkan
├── *.ipynb               # Notebook Jupyter untuk setiap analisis
└── README.md             # Dokumentasi proyek
```

## Persyaratan

- Python 3.x
- pandas
- numpy  
- scikit-learn
- NLTK
- TextBlob
- vaderSentiment
- afinn
- matplotlib
- seaborn

## Instalasi

```bash
pip install pandas numpy scikit-learn nltk textblob vaderSentiment afinn matplotlib seaborn
```

## Penggunaan

Analisis dilakukan dalam notebook Jupyter yang terpisah untuk setiap peristiwa bencana:

- `haiti_fix*.ipynb` - Analisis gempa Haiti
- `croatia_fix*.ipynb` - Analisis gempa Kroasia
- `catania_fix` - Analisis banjir Catania
- `eu_fix*.ipynb` - Analisis banjir Eropa Tengah

Setiap notebook mencakup seluruh proses mulai dari pra-pemrosesan data hingga evaluasi model.

## Hasil

Analisis ini menghasilkan klasifikasi sentimen serta metrik evaluasi untuk setiap peristiwa bencana menggunakan berbagai pendekatan analisis sentimen dan fungsi kernel SVM.

Hasil divisualisasikan menggunakan:

- Confusion matrix
- Perbandingan metrik kinerja
- Grafik distribusi sentimen