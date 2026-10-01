# Data dan batasan

Angka yang terlihat pada antarmuka adalah contoh untuk menguji susunan informasi dan interaksi. Jangan mengutipnya sebagai pengukuran lapangan.

## Node sensor

Daftar sepuluh node berada di array `nodes` dalam `app.js`. Setiap entri memiliki nama, ID, AQI, PM2.5, eCO2, TVOC, suhu, dan status. Filter Peta sensor menggunakan status `baik` atau `perhatian`. Pemilihan node mengubah panel detail, bukan sumber data.

## Analitik

Grafik memakai dua rangkaian koordinat statis untuk rentang 24 jam dan 7 hari. Kurva estimasi dimaksudkan untuk menjelaskan perbedaan pembacaan mentah dan hasil koreksi. Metrik model yang tampil juga merupakan contoh tampilan. Belum ada pelatihan model atau inferensi pada browser.

## Audit dan ekspor

Tabel audit berasal dari catatan contoh. Pilihan periode dan wilayah mengubah konteks laporan yang diunduh. CSV dan berkas spreadsheet memuat baris contoh, sedangkan laporan cetak dibuat dari halaman HTML yang dibuka untuk pencetakan. Nilai kepatuhan dan jejak karbon belum dihitung dari data aktivitas tervalidasi.

## Rekomendasi, chat, dan peringatan

Tombol `Saran lain` memilih salah satu teks lokal. AERO-BOT memilih jawaban berdasarkan kata kunci dari pertanyaan pengguna. Tombol `Tandai sudah dibaca` hanya mengubah keadaan halaman saat ini. Muat ulang halaman untuk kembali ke keadaan awal.

Sebelum integrasi produksi, tentukan ambang status, sumber waktu, satuan, metode koreksi, riwayat revisi data, dan siapa yang berwenang mengesahkan hasil audit.
