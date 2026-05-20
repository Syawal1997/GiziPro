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
*   **Premium UI/UX**: Menggunakan teknik Tailwind CSS tingkat lanjut seperti Glassmorphism (`backdrop-blur`), animasi gradient blob berjalan, shadow dinamis, dan efek *hover scaling*.
*   **Simulasi Database (LocalStorage)**: Karena proyek ini di-deploy sebagai *Static Site* di Vercel (yang tidak bisa memproses file `sqlite.db`), sistem menggunakan **LocalStorage API**.
    *   Fungsi CRUD (Create, Read, Update, Delete) beroperasi dengan sempurna pada menu **Kelola Pengguna** dan **Kelola Resep** di Panel Admin.
    *   Data tidak akan hilang saat browser di-refresh.
*   **Dashboard Modern SPA**: Transisi tab super halus tanpa *loading* dengan perhitungan ringkasan data yang merespon perubahan data pengguna/resep secara *real-time*.

## 💾 Catatan Tentang SQLite
Jika di masa depan Anda ingin menggunakan database **SQLite asli**, Anda harus meng-upgrade *stack* dari HTML Statis menjadi *Framework Backend* seperti:
1.  **Next.js** (Sangat disarankan jika menggunakan Vercel).
2.  **Node.js / Express** + Prisma ORM.
Untuk saat ini, metode *LocalStorage* adalah cara paling cerdas untuk mendemonstrasikan sistem ini bekerja secara *online* tanpa harus mengatur server backend di Vercel.

## 🛠️ Arsitektur File

1.  `index.html`: Landing page utama dengan penawaran paket dan informasi fitur.
2.  `login.html`: Gerbang autentikasi menuju panel sistem.
3.  `admin.html`: Dashboard operasional admin dengan fitur tab interaktif.

## 💻 Cara Deploy di Vercel

1.  Pastikan seluruh struktur file ini sudah di-commit di repositori GitHub Anda.
2.  Masuk ke dashboard Vercel > klik **Add New Project**.
3.  Pilih repositori ini, biarkan pengaturan tetap *default* (Framework: Other), dan klik **Deploy**.
4.  Jika ada *update* fitur di masa mendatang, cukup *commit* ulang ke cabang `main` di GitHub, dan Vercel akan langsung melakukan *auto-deployment*.
