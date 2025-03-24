# 📌 Project Pemweb dengan Docker

## 📂 Struktur Project
```
.
├── Readme.md
├── db
│   └── my.cnf
├── docker-compose.yml
├── nginx
│   ├── Dockerfile
│   └── default.conf
└── php
    ├── Dockerfile
    ├── docker-entrypoint.sh
    ├── local.ini
    └── www.conf
```

## 🚀 Cara Menjalankan Project

1️⃣ **Clone Repository**
```bash
git clone git@github.com:username/repository.git
cd repository
```

2️⃣ **Ganti isi `.env` dengan konfigurasi berikut:**
```ini
APP_TIMEZONE='Asia/Jakarta'
APP_URL=http://localhost
ASSET_URL=http://localhost
DB_HOST=db
DB_PASSWORD=p455w0rd
```

3️⃣ **Build dan Jalankan Container**
```bash
docker-compose up --build -d
```

4️⃣ **Cek container yang sedang berjalan**
```bash
docker ps
```

5️⃣ **Masuk ke dalam container PHP**
```bash
docker exec -it pemweb bash
```

6️⃣ **Jalankan perintah berikut dalam container**
```bash
php artisan key:generate
php artisan storage:link
php artisan migrate
chown -R www-data:www-data storage/*
chown -R www-data:www-data bootstrap/*
php artisan project:init
```

7️⃣ **Akses Website**
Buka browser dan akses:
```
http://localhost
```
Jika menggunakan server, akses dengan IP server di port 80.

8️⃣ **Stop dan Hapus Container**
```bash
docker-compose down
```

---

🎉 **Happy Coding from Elpun aka Elfan!** 🎉

📌 **Join Elpun Community:**  
[Discord](https://discord.gg/gMb8bt5e) | [YouTube](https://www.youtube.com/@Elpun378)

