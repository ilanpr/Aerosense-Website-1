# Pengembangan dan pemeriksaan

## Menjalankan lokal

Jalankan `python -m http.server 4173` dari akar repositori. Tidak ada langkah build. Perubahan HTML, CSS, atau JavaScript dapat diperiksa dengan memuat ulang halaman.

## Pemeriksaan sebelum commit

1. Buka keenam hash halaman: `#beranda`, `#peta`, `#analitik`, `#audit`, `#peringatan`, dan `#aerobot`.
2. Periksa menu pada layar desktop dan ponsel.
3. Pilih node peta, ganti filter, dan pastikan panel detail mengikuti pilihan.
4. Ganti rentang grafik, periode laporan, dan wilayah audit.
5. Unduh laporan contoh dan pastikan isi berkas sesuai pilihan.
6. Tandai peringatan sudah dibaca dan kirim pertanyaan AERO-BOT.
7. Periksa tampilan fokus keyboard dan pengaturan gerak minimal.

`node --check app.js` dapat dipakai untuk memeriksa sintaks JavaScript. Gambar pada README berada di `screenshots/` dan diambil dari situs yang dijalankan secara lokal.

## Integrasi berikutnya

Ganti nilai contoh melalui satu lapisan data yang memiliki penanganan loading dan kesalahan. Simpan kunci Gemini di server dan batasi informasi sensor yang diteruskan ke model. Simpan waktu pembacaan dan sumber data pada setiap catatan agar laporan audit dapat ditelusuri. Tambahkan pengujian alur end-to-end setelah layanan data terhubung.
