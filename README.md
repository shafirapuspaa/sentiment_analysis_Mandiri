# Livin' by Mandiri Sentiment Analysis

## 📌 Project Overview

Project ini merupakan analisis **sentiment pengguna terhadap aplikasi Livin' by Mandiri** berdasarkan review yang tersedia di Google Play Store.

Analisis dilakukan untuk memahami persepsi pengguna melalui kombinasi **rating pengguna dan sentiment dari teks review**, serta mengidentifikasi aspek yang mendapatkan respons positif maupun keluhan dari pengguna.

Project ini juga menganalisis perubahan pola rating dan sentiment pada periode munculnya **Issue A**, serta membedakan antara keluhan yang berkaitan dengan aplikasi dan respons pengguna terhadap isu eksternal.

---

## 🎯 Business Questions

Analisis ini dilakukan untuk menjawab beberapa pertanyaan bisnis:

1. Bagaimana persepsi pengguna terhadap aplikasi Livin' by Mandiri berdasarkan rating dan sentiment?
2. Apakah terdapat perubahan pola sentiment pengguna setelah Issue A?
3. Aspek apa yang mendapatkan respons positif dan perlu dipertahankan?
4. Aspek apa yang paling banyak dikeluhkan dan perlu diperbaiki?

---

## 📊 Dataset

Dataset berasal dari **Google Play Store reviews** aplikasi Livin' by Mandiri.

Dataset yang digunakan memiliki informasi seperti:

| Column | Description |
|---|---|
| `reviewId` | ID unik review |
| `userName` | Nama pengguna |
| `userImage` | URL gambar profil pengguna |
| `content` | Isi review |
| `score` | Rating pengguna (1–5) |
| `thumbsUpCount` | Jumlah helpful/upvote pada review |
| `reviewCreatedVersion` | Versi aplikasi ketika review dibuat |
| `at` | Tanggal dan waktu review |
| `replyContent` | Balasan developer |
| `repliedAt` | Waktu balasan developer |
| `appVersion` | Versi aplikasi |

Analisis difokuskan pada review tahun **2026**.

---

## 🔎 Data Preprocessing

Tahapan preprocessing yang dilakukan meliputi:

- Mengubah teks menjadi lowercase
- Membersihkan punctuation dan karakter yang tidak diperlukan
- Membersihkan whitespace
- Normalisasi beberapa kata slang dan typo
- Mengubah emoji menjadi representasi teks menggunakan emoji dictionary
- Mempertahankan kata-kata yang memiliki informasi sentiment
- Filtering data berdasarkan periode analisis

Emoji tidak langsung dihapus, tetapi dikonversi menjadi teks agar informasi sentiment dari emoji tetap dapat digunakan dalam proses klasifikasi.

---

## 🏷️ Sentiment Labeling Based on Rating

Rating digunakan sebagai dasar untuk membuat label sentiment:

| Rating | Sentiment |
|---:|---|
| 1 | Negative |
| 2 | Negative |
| 3 | Negative |
| 4 | Positive |
| 5 | Positive |

