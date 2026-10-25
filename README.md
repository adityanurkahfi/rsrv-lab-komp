# Reservasi Lab Komputer

Halaman statis untuk membuka aplikasi Reservasi Lab Komputer dari Google Apps Script. `index.html` langsung memuat aplikasi dalam iframe, tanpa proses build, JavaScript tambahan, atau layar loading pada halaman ini.

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

- Tidak ada dependensi atau perintah build untuk halaman ini. URL Google Apps Script ada pada atribut `src` iframe di `index.html`; ubah URL tersebut jika deployment Apps Script berganti.
- Halaman yang diterbitkan tetap memerlukan koneksi ke Google Apps Script. Jika isi iframe tidak muncul, periksa akses deployment Apps Script dan izin untuk ditampilkan dalam iframe. Loading yang berasal dari aplikasi Apps Script perlu diubah pada kode aplikasi tersebut.
