# Backend Project - PERN Stack (Drizzle ORM & Better Auth)

Ini adalah layanan backend untuk aplikasi manajemen akademik yang dibangun menggunakan Node.js, Express, dan PostgreSQL. Proyek ini menggunakan Drizzle ORM untuk manajemen database dan Better Auth untuk sistem autentikasi.

## 🚀 Fitur Utama

- **Autentikasi & Otorisasi**: Menggunakan `better-auth` untuk manajemen user.
- **Manajemen Akademik**: API untuk mengelola Departemen, Mata Pelajaran (Subjects), Kelas, dan Pendaftaran (Enrollments).
- **Statistik**: Endpoint khusus untuk menyediakan data statistik.
- **Database ORM**: Menggunakan Drizzle ORM dengan PostgreSQL (Neon DB).
- **Type Safety**: Dibangun menggunakan TypeScript.
- **Monitoring**: Terintegrasi dengan ManageEngine APM Insight.

## 🛠️ Stack Teknologi

- **Runtime**: Node.js
- **Framework**: Express.js (v5)
- **Bahasa**: TypeScript
- **Database**: PostgreSQL (Neon Database)
- **ORM**: Drizzle ORM
- **Autentikasi**: Better Auth
- **Security**: Arcjet, CORS
- **Development Tool**: tsx, drizzle-kit

## 📋 Prasyarat

Sebelum menjalankan proyek ini, pastikan Anda telah menginstal:
- [Node.js](https://nodejs.org/) (versi terbaru disarankan)
- [npm](https://www.npmjs.com/) atau [yarn](https://yarnpkg.com/)
- Akun [Neon Console](https://neon.tech/) untuk database PostgreSQL (atau PostgreSQL lokal)

## ⚙️ Konfigurasi Environment

Buat file `.env` di root direktori proyek dan tambahkan variabel berikut:

```env
PORT=8000
DATABASE_URL=your_postgresql_connection_string
FRONTEND_URL=http://localhost:5173
BETTER_AUTH_SECRET=your_auth_secret
BETTER_AUTH_URL=http://localhost:8000
```

## 🚀 Cara Menjalankan Project

### 1. Instalasi Dependensi
```bash
npm install
```

### 2. Persiapan Database
Jalankan perintah berikut untuk menghasilkan migrasi dan menerapkannya ke database:

```bash
# Generate migrasi berdasarkan skema
npm run db:generate

# Terapkan migrasi ke database
npm run db:migrate

# (Opsional) Seed data awal
npm run db:seed
```

### 3. Menjalankan Mode Development
```bash
npm run dev
```
Server akan berjalan di `http://localhost:8000`.

### 4. Build dan Production
Untuk menjalankan dalam mode production:

```bash
# Compile TypeScript ke JavaScript
npm run build

# Jalankan server hasil build
npm run start
```

## 📁 Struktur Proyek

- `src/index.ts`: Entry point aplikasi.
- `src/db/`: Konfigurasi database dan skema Drizzle.
- `src/routes/`: Definisi API endpoints.
- `src/lib/`: Library pendukung (seperti konfigurasi auth).
- `seed/`: Skrip untuk pengisian data awal database.
- `drizzle/`: File migrasi database yang dihasilkan oleh Drizzle Kit.

## 🛣️ API Endpoints Utama

- `/api/auth/*`: Endpoint autentikasi (Better Auth).
- `/api/departments`: Manajemen departemen.
- `/api/subjects`: Manajemen mata pelajaran.
- `/api/classes`: Manajemen kelas.
- `/api/enrollments`: Manajemen pendaftaran mahasiswa ke kelas.
- `/api/users`: Manajemen data pengguna.
- `/api/stats`: Data statistik aplikasi.

---
Dibuat untuk mempermudah pengelolaan data akademik secara efisien.
