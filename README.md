<h1 align="center">Aplikasi pendataan jalan lingkungan</h1>

Aplikasi sederhana untuk mencatat dan mengelola data jalan lingkungan berdasarkan kelurahan dan kecamatan.

### requirment
1. php 8.3 
2. laravel 13
3. MySQL

### langkah-langkah instalasi
1. clone repositorynya 
2. buka cmd di folder projectnya, lalu ketik `composer install` untuk instal dependensinya
3. salin file `.env.example` setelah itu rename menjadi `.env`
4. buka file `.env` yang baru saja di rename, edit databasenya di:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=tes_pkl_jalan
   DB_USERNAME=root
   DB_PASSWORD=
5. setelah selesai mengedit file `.env` jalankan perintah berikut:
```bash
php artisan key:generate
```
6. jalankan migrate dan seeder untuk membuat tabel dan datanya:
```bash
php artisan migrate:fresh --seed
```


   
