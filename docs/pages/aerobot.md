# Tanya AERO-BOT

AERO-BOT dirancang untuk menjelaskan kondisi udara dengan kalimat singkat dalam bahasa Indonesia.

## Isi halaman

Panel percakapan berisi sapaan awal, pilihan pertanyaan, area pesan, dan kolom untuk menulis pertanyaan. Panel perkenalan memakai ilustrasi robot, sedangkan daftar topik menjelaskan jenis pertanyaan yang dapat diajukan.

## Interaksi

- Pilih pertanyaan awal atau ketik pesan sendiri.
- Pesan pengguna masuk ke riwayat percakapan.
- Jawaban muncul setelah jeda singkat.
- Topik yang dikenal mencakup AQI, PM2.5, eCO2, kondisi kawasan, serta beberapa lokasi node.

Jawaban berasal dari aturan kata kunci di `app.js`, bukan dari Gemini. Untuk menghubungkan Gemini, kirim pesan melalui endpoint server, sertakan konteks sensor yang tervalidasi, dan tampilkan waktu sumber data dalam jawaban. Saran kesehatan tetap bersifat umum; keluhan kesehatan perlu ditangani oleh tenaga kesehatan.
