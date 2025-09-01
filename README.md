# 📊 Analisis Sentimen Pengguna Aplikasi GoPay

### *Studi Kasus: Membedah Ulasan Pengguna pada Versi Aplikasi 4.0.0 - 4.9.3*

---

### 📂 Ikhtisar Proyek (Project Overview)

GoPay adalah salah satu dompet digital terdepan di Indonesia, dengan jutaan pengguna yang berinteraksi setiap hari. Namun, di balik angka-angka besar tersebut, bagaimana sebenarnya perasaan pengguna terhadap aplikasi ini, terutama saat terjadi siklus pembaruan fitur yang intensif?

Proyek ini melakukan penyelaman mendalam (*deep dive*) ke dalam **ribuan ulasan pengguna GoPay di Google Play Store**, dengan fokus spesifik pada rentang **versi aplikasi 4.0.0 hingga 4.9.3**. Tujuannya adalah untuk mengubah ulasan kualitatif menjadi wawasan kuantitatif yang dapat ditindaklanjuti. Dengan memanfaatkan analisis sentimen berbasis AI, kita dapat mengungkap:
* **Pola sentimen** pengguna secara keseluruhan (Positif, Negatif, Netral).
* **Topik utama** yang mendorong kepuasan dan kekecewaan.
* **Rekomendasi strategis** untuk siklus pengembangan produk selanjutnya.

---

### 🔗 Tautan Dataset Mentah (Raw Dataset Link)

* **Sumber Data:** Kaggle
* **Nama Dataset:** Gojek App Reviews (Bahasa Indonesia)
* **Tautan:** `https://www.kaggle.com/datasets/ucupsedaya/gojek-app-reviews-bahasa-indonesia`
* **Presentation Slide:** `https://www.canva.com/design/DAGxtmRjlgo/8DeLHu9dCiiYAvMbJeIVZw/edit?utm_content=DAGxtmRjlgo&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton`

---

### 🎯 Wawasan & Temuan Utama (Insight & Findings)

Analisis pada 400 sampel ulasan dari versi 4.x mengungkapkan sebuah cerita yang terpolarisasi:

#### **Gambaran Besar: Mayoritas Puas, Tapi Minoritas Bersuara Keras**
Dari segi angka, sentimen pengguna cenderung **positif (~56%)**. Namun, ada kelompok pengguna yang signifikan dan vokal yang memberikan ulasan **negatif (~38%)**. Ini menunjukkan bahwa meskipun produk ini bekerja dengan baik untuk sebagian besar orang, ada masalah serius yang dialami oleh sebagian lainnya.

> #### 👍 Yang Disukai Pengguna: Kecepatan & Kemudahan
> Ulasan positif secara konsisten menyoroti efisiensi GoPay. Kata-kata seperti **"mudah", "cepat", "lancar",** dan **"sangat membantu"** mendominasi. Ini menegaskan bahwa GoPay berhasil memenuhi janji utamanya sebagai alat transaksi yang praktis.
>
> #### 👎 Yang Dikeluhkan Pengguna: Stabilitas & Masalah Teknis
> Di sisi lain, ulasan negatif hampir seluruhnya berpusat pada masalah teknis. Kata **"error"** menjadi tema utama, diikuti oleh keluhan terkait aplikasi yang **"lama", "susah login",** dan masalah pada **"saldo"**. Kata **"update"** yang sering muncul menandakan bahwa pembaruan aplikasi seringkali menjadi pemicu masalah ini.

**Kesimpulan Inti:** Ada pertarungan antara **konsep produk yang hebat** (transaksi mudah) dan **eksekusi teknis yang kurang stabil**. Pengguna menyukai apa yang GoPay tawarkan, tetapi frustrasi dengan pengalaman pengguna yang sering terganggu oleh *bug* dan masalah performa.

---

### 🤖 Penjelasan Dukungan AI (AI Support Explanation)

Analisis ini tidak akan mungkin dilakukan dalam skala dan kecepatan seperti ini tanpa dukungan Kecerdasan Buatan (AI).

* **Model yang Digunakan:** **`ibm-granite/granite-3.3-8b-instruct`** melalui platform Replicate.
* **Peran AI:** Model AI bertindak sebagai seorang analis data yang tak kenal lelah. Ia membaca setiap ulasan yang diberikan, memahami konteksnya dalam Bahasa Indonesia, dan secara otomatis mengklasifikasikannya ke dalam sentimen **Positif, Negatif, atau Netral**.
* **Manfaat:** Proses yang jika dilakukan manual akan memakan waktu berjam-jam dan rentan terhadap subjektivitas, dapat diselesaikan oleh AI dalam hitungan menit dengan tingkat konsistensi yang tinggi. Ini memungkinkan kita untuk fokus pada interpretasi hasil dan pembuatan strategi.
