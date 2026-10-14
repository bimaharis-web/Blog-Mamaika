# Menyiapkan Admin Blog Mamaika

Panel admin memakai Decap CMS dan Decap Turbo untuk autentikasi serta akses GitHub. Jangan menaruh access token atau password di file konfigurasi blog.

## Membuat site Decap Turbo

1. Daftar atau masuk di [Decap Turbo](https://turbo.decapcms.org/signup).
2. Di organisasi Turbo, buka **Git connection**, hubungkan GitHub, dan izinkan GitHub App mengakses repo `bimaharis-web/Blog-Mamaika`.
3. Buat site baru dengan pengaturan:
   - **Site name:** Blog Mamaika
   - **Git provider:** GitHub
   - **Repo:** `bimaharis-web/Blog-Mamaika`
   - **Branch:** `main`
   - **Config path:** `admin/config.yml`
   - **Admin interface URL:** `https://blog.mamaika.my.id/admin/`
4. Salin **Site ID** dari tab **Overview**.
5. Ganti `REPLACE_WITH_DECAP_TURBO_SITE_ID` pada `backend.turbo_site_id` di `admin/config.yml` dengan Site ID tersebut, lalu commit ke branch `main`.
6. Setelah GitHub Pages selesai deploy, buka `https://blog.mamaika.my.id/admin/` dan masuk dengan akun Decap Turbo yang memiliki akses ke site.

## Menulis artikel

Di panel admin, buka **Artikel → New Artikel**. Isi judul, tanggal terbit, kategori, ringkasan, gambar, deskripsi gambar, dan isi artikel. Simpan untuk menerbitkan perubahan ke `main`; GitHub Pages akan membangun ulang blog secara otomatis.

Paket gratis Decap Turbo saat ini menyediakan satu site dan satu seat. Periksa halaman paket Decap Turbo untuk ketentuan terbaru.
