# Arsitektur

AEROSENSE saat ini adalah situs statis. Semua halaman berada di `index.html`, dengan satu berkas JavaScript untuk navigasi dan interaksi. Tidak ada framework, bundler, atau layanan backend yang diperlukan untuk menjalankannya.

## Alur halaman

Menu samping menggunakan atribut `data-view`. Fungsi `showView` di `app.js` menampilkan satu section yang sesuai, memperbarui label breadcrumb, dan menyimpan nama halaman di hash URL. Tautan seperti `#peta` dan `#aerobot` dapat dibuka langsung. Menu pada layar sempit memakai tombol dengan status `aria-expanded`.

## Pembagian berkas

- `index.html`: struktur halaman, teks, ikon SVG internal, dan elemen semantik.
- `styles.css`: dasar tampilan, komponen bersama, grid, dan breakpoint responsif.
- `dashboard-refinement.css`: penyesuaian panel utama, kartu rekomendasi, dan ilustrasi.
- `app.js`: data contoh, navigasi, filter node, pilihan grafik, ekspor, status peringatan, dan percakapan.
- `assets/`: karya visual lokal agar antarmuka tidak bergantung pada gambar eksternal.

Satu-satunya permintaan eksternal saat halaman dibuka adalah font Inter dari Google Fonts. Sistem font cadangan tetap digunakan jika font tersebut tidak tersedia.

## Arah integrasi

Integrasi telemetri sebaiknya menyediakan ID node, lokasi, nilai sensor, satuan, status, dan waktu pembacaan yang jelas. Data mentah dan hasil koreksi perlu dipisahkan. Untuk AERO-BOT, permintaan Gemini harus melewati server agar kunci API tidak tersimpan dalam kode browser. Penyimpanan audit dan status peringatan memerlukan backend jika keduanya harus bertahan antar sesi atau dipakai oleh beberapa pengguna.
