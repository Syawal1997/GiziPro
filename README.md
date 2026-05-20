# GiziPro 🌱

GiziPro adalah *landing page* dan *dashboard* modern yang dirancang untuk platform analisis kebutuhan gizi cerdas. Proyek ini dibangun sepenuhnya di ranah *frontend* dengan simulasi fungsionalitas logika bisnis menggunakan JavaScript murni.

## 🚀 Fitur Terbaru

*   **Desain Responsif & Animasi**: UI bersih dengan elemen interaktif seperti *Carousel Testimonial* berbasis CSS Scroll Snap dan animasi *hover state* menggunakan Tailwind CSS.
*   **Sistem Autentikasi (Mock Login)**: Dilengkapi halaman `login.html` dengan keamanan level *session storage* browser. 
    *   **Kredensial Login Admin**: 
        *   Username: `syawal`
        *   Password: `syawal123`
*   **Dashboard SPA (Single Page Application)**: Halaman `admin.html` yang merender konten antar-menu (Dashboard, Pengguna, Resep, Transaksi, Laporan, Pengaturan) secara dinamis tanpa *reload* halaman menggunakan Vanilla JS.
*   **Keamanan Rute Sederhana**: Script pencegah masuk ke halaman admin apabila sesi belum terdaftar (ter-logout).

## 🛠️ Arsitektur File

1.  `index.html`: Landing page utama dengan penawaran paket dan informasi fitur.
2.  `login.html`: Gerbang autentikasi menuju panel sistem.
3.  `admin.html`: Dashboard operasional admin dengan fitur tab interaktif.

## 💻 Cara Deploy di Vercel

1.  Pastikan seluruh struktur file ini sudah di-commit di repositori GitHub Anda.
2.  Masuk ke dashboard Vercel > klik **Add New Project**.
3.  Pilih repositori ini, biarkan pengaturan tetap *default* (Framework: Other), dan klik **Deploy**.
4.  Jika ada *update* fitur di masa mendatang, cukup *commit* ulang ke cabang `main` di GitHub, dan Vercel akan langsung melakukan *auto-deployment*.
