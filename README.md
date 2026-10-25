# Reservasi Lab Komputer

Halaman statis yang langsung mengalihkan pengunjung ke aplikasi Reservasi Lab Komputer di Google Apps Script. Tidak ada proses build, JavaScript, atau animasi loading pada halaman ini.

## Deploy ke Cloudflare Pages

1. Simpan `index.html` dan `README.md` di akar repositori Git.
2. Di Cloudflare, buka **Workers & Pages → Create application → Pages → Import an existing Git repository** dan pilih repositori ini.
3. Pilih branch produksi. Gunakan **Framework preset: None**, **Build command: `exit 0`**, dan **Build output directory: `.`** (akar repositori).
4. Deploy, lalu buka URL `*.pages.dev` yang diberikan Cloudflare.

## Deploy ke GitHub Pages

1. Push berkas di akar repositori ke GitHub.
2. Buka **Settings → Pages** pada repositori.
3. Pada **Build and deployment**, pilih **Deploy from a branch**, lalu pilih branch yang berisi `index.html` dan folder **/(root)**. Simpan pengaturan.
4. Buka URL Pages yang ditampilkan GitHub setelah publikasi selesai.

## Catatan

- URL Google Apps Script ada pada tag `meta http-equiv="refresh"` dan tautan cadangan di `index.html`. Perbarui keduanya jika deployment Apps Script berganti.
- Alamat Cloudflare Pages atau GitHub Pages akan mengalihkan browser ke domain `script.google.com`. Ini diperlukan karena Google Apps Script saat ini menolak ditampilkan di iframe dari domain lain.
- Halaman tetap memerlukan akses ke Google Apps Script. Jika aplikasinya tidak terbuka secara langsung, periksa akses dan status deployment Apps Script.
