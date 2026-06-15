# ChatAI DPRD Sumenep

Aplikasi AI asisten untuk DPRD Sumenep — berbasis web, dibangun sebagai **single-file standalone HTML** (semua CSS, JavaScript, dan aset sudah di-inline dalam satu file `index.html`). Tidak membutuhkan build step, tidak membutuhkan server backend, dan tidak membutuhkan dependensi eksternal.

---

## Deploy ke Vercel

### Opsi A — Vercel CLI (Terminal)

```bash
# 1. Install Vercel CLI (sekali saja)
npm install -g vercel

# 2. Login ke akun Vercel
vercel login

# 3. Deploy preview (dari folder project ini)
vercel

# 4. Deploy ke production
vercel --prod
```

Setelah `vercel --prod`, Anda akan mendapat URL production seperti:
`https://chatai-dprd-sumenep.vercel.app`

---

### Opsi B — Import dari GitHub (Dashboard Vercel)

1. Buka [vercel.com/new](https://vercel.com/new) dan login.
2. Klik **"Import Git Repository"** → pilih repo `ChatAI-DPRD-SUMENEP`.
3. Di halaman konfigurasi:
   - **Framework Preset**: pilih `Other`
   - **Build Command**: kosongkan (biarkan blank)
   - **Output Directory**: `.` (titik — root folder)
   - **Install Command**: kosongkan
4. Klik **Deploy**.

Vercel otomatis mendeteksi `vercel.json` dan melayani `index.html` sebagai static site.

---

## Catatan Teknis

- Ini adalah **static single-file app** — tidak ada server, tidak ada database, tidak ada build pipeline.
- File `index.html` adalah bundle lengkap; semua aset di-embed sebagai base64 di dalam file.
- Setiap push ke branch `main` di GitHub akan otomatis trigger re-deploy (jika sudah dihubungkan via Opsi B).
- Tidak ada API key yang tersimpan di source code.
