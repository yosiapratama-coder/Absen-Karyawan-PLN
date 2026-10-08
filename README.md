# Sistem Absensi PT PLN (Persero) UIP3B Sumatera

Fitur:
- Akses web melalui HP/laptop.
- Kamera browser.
- Verifikasi wajah menggunakan face descriptor.
- Absen masuk/pulang.
- Waktu otomatis.
- Data tersimpan otomatis di Firebase Firestore.
- Halaman admin untuk pendaftaran wajah dan melihat 100 riwayat terakhir.

## Setup
1. Buat project di Firebase Console.
2. Aktifkan Firestore Database.
3. Buat Web App dan salin konfigurasi ke `firebase-config.js`.
4. Terapkan rules dari `firestore.rules` untuk DEMO.
5. Upload seluruh folder ke hosting HTTPS (Firebase Hosting, Vercel, Netlify, GitHub Pages, dll).
6. Buka `admin.html`, aktifkan kamera, masukkan NIK + nama, lalu daftarkan wajah.
7. Karyawan dapat membuka `index.html` dan melakukan absensi.

## Penting untuk produksi
Rules demo sengaja longgar agar bisa langsung diuji. Jangan digunakan untuk data pegawai sungguhan tanpa:
- Firebase Authentication dan role admin.
- Pembatasan read/write Firestore.
- HTTPS.
- Liveness / anti-spoofing.
- Kebijakan retensi dan perlindungan data biometrik.
- Audit log dan pembatasan perubahan data.
- Pertimbangan kepatuhan UU PDP dan kebijakan keamanan PLN.

Face descriptor adalah data biometrik sensitif; jangan menganggap sistem browser ini sebagai pengganti sistem biometrik enterprise.
