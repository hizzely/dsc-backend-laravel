# Intro Framework Laravel @ DSC JogFest 2020

Repository ini adalah kode project yang dibuat saat workshop Learning Path Backend: Framework Laravel pada 12 Desember 2020 dengan sedikit improvisasi.

## Get Started with Laravel Sail (Docker)
1. Clone (download) project ini kemudian ekstrak dan masuk ke direktori tersebut.
2. Install semua dependensi:
```
$ docker run --rm \
      -v $(pwd):/opt \
      -w /opt \
      laravelsail/php80-composer:latest \
      composer install
```
3. Dan project bisa langsung dijalankan dengan:
```
$ ./vendor/bin/sail up
```

## Get Started with Composer
1. Install PHP dan MySQL, agar lebih simpel bisa install Laragon / XAMPP / MAMP.
2. Install [Composer](https://getcomposer.org).
3. Pastikan PHP bisa diakses lewat Command Prompt atau Terminal dengan mendaftarkannya ke Environment Variables. Cek dengan:
```
$ php  -v
$ composer -V
```
4. Clone (download) project ini kemudian ekstrak dan masuk ke direktori tersebut.
5. Install semua dependensi:
```
$ composer install
```
6. Start service PHP dan MySQL, jika menggunakan Laragon / XAMPP / MAMP bisa distart juga Web Servernya.
7. Jalankan project dengan:
```
$ php artisan serve
```

## Initial Configuration
1. Duplikat file `.env.example` dan ganti namanya menjadi `.env`.
2. Buka Command Prompt atau Terminal dengan posisi current directory ada di project.
3. Jalankan perintah berikut untuk generate app key, jika menggunakan Docker:
```
## Jika menggunakan Laravel Sail
$ vendor/bin/sail artisan key:generate

## Jika tidak menggunakan Laravel Sail
$ php artisan key:generate
```
4. Buat database kosong, nama bisa bebas. Teman-teman bisa membuatnya langsung lewat console MySQL atau lewat tool seperti phpMyAdmin, MySQL Workbench, Navicat, dll.
5. Perbarui detail database yang ada di file `.env` agar sesuai dengan database yang sudah dibuat. Selain nama database, jika menggunakan Laragon / XAMPP / MAMP, server: `localhost` username: `root` dan password dikosongi.
6. Jalankan migrasi untuk mempersiapkan database:
```
## Jika menggunakan Laravel Sail
$ vendor/bin/sail artisan key:generate

## Jika tidak menggunakan Laravel Sail
$ php artisan key:generate
```

## Background
Materi belajar Laravel sangat banyak di Internet, mulai dari yang dasar hingga advanced dan dari yang gratis hingga berbayar. Tapi pastinya akan ada gap yang dirasakan ketika tiba-tiba langsung belajar framework, terutama buat kamu yang baru banget belajar pemrograman PHP.  

Goal dari materi workshop dan project yang saya bawakan adalah untuk membantu teman-teman memperkecil gap tersebut ketika melakukan transisi dari menggunakan PHP secara native (tanpa framework) menjadi menggunakan framework.

## Scope Workshop
- Kenapa kita menggunakan Framework?
- Kenapa Laravel?
- Gimana Cara Memulai Project Laravel?
- Ngulik Laravel
- Diskusi

## Scope Project
- Setup project Laravel baru via Laravel Sail (Docker) dan Composer.
- Intro: Composer, Konfigurasi Project, Routing, Controller, Model & Eloquent ORM, View & Blade, DB Migration, Request Validation.
- Implementasi CRUD sederhana dengan interface REST API.

## What's Next?
- [Laravel](https://laravel.com) - Laravel dan Ekosistemnya 
- [Laravel Docs](https://laravel.com/docs) - Buat kamu yang pengen mendalami Laravel.
- [Laracasts](https://laracasts.com) - Buat kamu yang pengen belajar Laravel tapi ngantuk kalo baca.
- [Backend Dev Roadmap](https://roadmap.sh/backend) - Buat kamu yang pengen mendalami backend lebih jauh.

## Let's Connect!
Saya Rohmad, seorang yang masih butuh banyak belajar seperti teman-teman. Yuk kita belajar bareng! Teman-teman dapat [menghubungi saya disini](https://linktr.ee/rfajar) ;)