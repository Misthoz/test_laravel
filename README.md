referensi readme

# Sistem Pendataan Jalan Lingkungan

Aplikasi sederhana untuk mencatat dan mengelola data jalan lingkungan berdasarkan kelurahan dan kecamatan. Aplikasi ini dikembangkan untuk memenuhi tugas Paket B.

## Persyaratan Sistem
- PHP >= 8.2
- Laravel 11.x
- MySQL / MariaDB

## Langkah Instalasi
1. Clone repository ini.
2. Jalankan perintah `composer install` untuk menginstal dependensi.
3. Salin file `.env.example` menjadi `.env`:
   ```bash
   cp .env.example .env
   ```
4. Atur koneksi database pada file `.env`:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=tes_pkl_jalan
   DB_USERNAME=root
   DB_PASSWORD=
   ```
5. Generate application key:
   ```bash
   php artisan key:generate
   ```
6. Jalankan migrasi dan seeder untuk membuat tabel dan data awal:
   ```bash
   php artisan migrate:fresh --seed
   ```

## Cara Menjalankan Aplikasi
Jalankan development server lokal dengan perintah:
```bash
php artisan serve
```
Buka browser dan akses `http://localhost:8000`.

## Daftar Fitur
### Fitur yang berhasil dibuat:
- [x] Relasi database (Kecamatan, Kelurahan, Jalan) dengan Foreign Key yang aman (restrictOnDelete).
- [x] CRUD Kecamatan (Create, Read, Update, Delete) + Detail.
- [x] CRUD Kelurahan + Detail.
- [x] CRUD Jalan + Detail.
- [x] Validasi form di backend.
- [x] Pencarian data jalan berdasarkan nama.
- [x] Filter data jalan berdasarkan kondisi dan jenis permukaan.
- [x] Ringkasan data (total jalan, kondisi baik, rusak ringan, rusak berat, total panjang).
- [x] Desain responsif menggunakan Bootstrap 5.
- [x] Error handling saat menghapus data induk yang masih memiliki relasi.
- [x] Pagination.
- [x] Soft Deletes.
- [x] Tombol reset pencarian.

### Fitur yang belum selesai:
- Tidak ada.

## Catatan
Aplikasi ini dikembangkan dengan bantuan AI (Antigravity/Claude/Gemini) untuk:
- Implementasi cepat desain antarmuka menggunakan Bootstrap 5.
- Melengkapi fungsi CRUD, search, filter, dan perhitungan ringkasan di Controller.
- Implementasi handling QueryException saat penghapusan foreign key (restrictOnDelete).
