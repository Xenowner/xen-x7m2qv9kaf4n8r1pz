# Good Night — Cara Pasang ke GitHub Pages

Folder ini isinya udah lengkap siap upload, nggak perlu diedit lagi.

## Langkah cepat

1. Bikin repository baru di GitHub (public atau private, bebas)
2. Upload **semua file di folder ini apa adanya** (`index.html`, `manifest.json`, `service-worker.js`, `icon-192.png`, `icon-512.png`, `splash-full.png`) ke root repo — semuanya flat, nggak ada subfolder
3. Masuk ke **Settings → Pages**
4. Di bagian **Source**, pilih branch `main` dan folder `/ (root)`, klik **Save**
5. Tunggu 1-2 menit, nanti aktif di `https://username-kamu.github.io/nama-repo/`

## Install ke layar utama HP

1. Buka link GitHub Pages kamu di Chrome (Android) atau Safari (iPhone)
2. Chrome: menu titik tiga → **"Instal aplikasi"** / **"Tambahkan ke layar utama"**
   Safari: tombol Share → **"Add to Home Screen"**
3. Ikon aplikasinya bakal pakai foto yang udah di-crop penuh (nggak ada bar hitam), dan pas dibuka bakal muncul splash screen foto itu juga sebentar sebelum masuk ke app-nya

## Kalau nanti update kode

Tiap kali kamu edit `index.html` dan upload ulang ke GitHub, buka `service-worker.js`, naikkan angka di baris:
```js
const CACHE_VERSION = 'goodnight-v1';
```
jadi `'goodnight-v2'`, dst. Ini penting — kalau nggak dinaikkan, HP yang udah nge-install PWA-nya bakal tetep pakai versi lama yang ke-cache, nggak otomatis update.
