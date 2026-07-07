# Desain dan Analisis Algoritma (DAA)

Repository ini berisi portofolio pembelajaran mata kuliah **Desain dan Analisis Algoritma** — mencakup diagram UML, analisis sistem, dan implementasi aplikasi web menggunakan **Laravel Filament** dengan **Docker**.

---

## Struktur Folder

| Folder | Deskripsi |
|---|---|
| `pert1/` | Sequence diagram menu menggunakan PlantUML |
| `pert2/` | Use case diagram sistem restoran + sample app Laravel (Docker: PHP, MariaDB, Nginx) |
| `pert3/` | Sample app Laravel dengan Docker |
| `pert10/` | Laravel Filament starter dengan model **Product** & **Kategori** (relasi belongsTo/hasMany), migrasi, seeder |
| `uts/` | Ujian Tengah Semester — analisis dan sample app |
| `uas/` | **Sistem Pengaduan Masyarakat Berbasis Web** — use case, flowchart, schema DB (users, pengaduans, notifikasis), analisis Laravel Filament + Docker |
| `projectUAS/` | **PT. Meowrigin** — sistem manajemen atlet biliar (8-ball & 9-ball), analisis SWOT, LTAD, klasifikasi penilaian atlet (Kategori A/B/C), protokol cedera |

---

## Teknologi

- **Backend**: Laravel (Filament untuk admin panel)
- **Database**: MariaDB
- **Web Server**: Nginx
- **Containerization**: Docker (PHP-FPM, MariaDB, Nginx)
- **Diagram**: PlantUML

---

## Cara Menjalankan Sample App

Setiap sample app (`pert2`, `pert3`, `pert10`, `uts`, `uas`) dapat dijalankan dengan:

```bash
cd <folder>/sampleapp
docker compose up -d
docker exec -it sample bash
composer install
php artisan key:generate
php artisan migrate --seed
```

Akses di `http://localhost`.

---

## Studi Kasus UAS

### 1. Sistem Pengaduan Masyarakat
Media pelaporan infrastruktur warga ke Kelurahan A. Masyarakat dapat mengajukan pengaduan dengan foto & lokasi; admin memverifikasi dan meneruskan ke instansi terkait.

### 2. PT. Meowrigin (Billiard Academy)
Perusahaan pelatihan biliar fokus regenerasi atlet muda. Sistem mencakup:
- Penilaian atlet (teknik, taktik, mental, fisik) skala 1–5
- Kategori atlet: A (siap bertanding), B (perlu pembinaan), C (pengembangan signifikan)
- Manajemen jadwal latihan & turnamen
- Protokol penanganan cedera atlet
