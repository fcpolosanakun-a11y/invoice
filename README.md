# 🎀 Chubbysstrey Invoice Maker — versi Netlify

| File | Fungsi |
|---|---|
| `index.html` | Aplikasi (21 desain, 15 palet, 19 font) |
| `data.json` | **Pengaturan awal** yang bisa kamu edit |
| `netlify.toml` | Konfigurasi Netlify (jangan diubah) |
| `assets/` | Chibi asli (`chibi1.jpg`, `chibi2.jpg`, `chibi3.jpg`) |

## Edit `data.json`
- `shop`, `tag`, `wa`, `x`, `tg`: nama toko, tagline, WhatsApp, X, Telegram (tanpa @)
- `pay`, `est`, `note`: metode bayar, estimasi, catatan awal
- `f1`, `f2`, `f3`: font judul / miring / teks (nama font persis seperti di pilihan Font)
- `lay` (0-20) bentuk invoice, `th` (0-14) palet, `ch` (0-2) chibi, `pos` (`top`/`side`/`bottom`/`wm`), `size`, `op`
- `chibi`: daftar file gambar chibi
Hati-hati: JSON harus pakai tanda kutip dua `"` dan tanpa koma di item terakhir.
Pengaturan ini dipakai kalau browser belum pernah menyimpan data. Untuk reset: hapus data situs di browser.

## Cara 1 — Drag & drop (paling mudah, tanpa GitHub)
1. Ekstrak ZIP.
2. Buka https://app.netlify.com/drop (login dulu).
3. Seret **folder hasil ekstrak** (yang berisi `index.html`) ke halaman itu.
4. Selesai, website langsung online di `https://xxxx.netlify.app`. Ganti nama di Site configuration → Change site name.
Update: buka project → **Deploys** → seret folder lagi.

## Cara 2 — Lewat GitHub (update otomatis)
1. Buat repository baru di GitHub, upload semua isi folder (`index.html` harus di paling luar).
2. Netlify → **Add new site → Import an existing project → GitHub** → pilih repo.
3. Build command **kosong**, Publish directory `.` (sudah diatur `netlify.toml`) → **Deploy**.
4. Setiap kamu edit `data.json` di GitHub, Netlify deploy ulang otomatis.

## Masalah umum
- Chibi tidak muncul: cek path di `data.json` dan nama file di `assets/`.
- Pengaturan tidak berubah: kemungkinan browser menyimpan data lama, hapus data situs lalu refresh.
- Jangan buka `index.html` langsung dari file (double-click) untuk membaca `data.json`; pakai versi online atau server lokal.
