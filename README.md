# Vanguard - Modern Full-Stack Boilerplate dengan Go dan React
Boilerplate full-stack Go dan React dengan integrasi RBAC

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Go](https://img.shields.io/badge/Go-v1.24-blue.svg)
![Gin](https://img.shields.io/badge/Gin-v1.9+-darkblue.svg)
![GORM](https://img.shields.io/badge/GORM-v1.25+-brightgreen.svg)
![Zerolog](https://img.shields.io/badge/Zerolog-v1.30+-green.svg)
![React](https://img.shields.io/badge/React-v18+-lightblue.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-v5+-blueviolet.svg)
![Vite](https://img.shields.io/badge/Vite-v4+-purple.svg)
![SWC](https://img.shields.io/badge/SWC-brightgreen.svg)
![RBAC](https://img.shields.io/badge/RBAC-yellowgreen.svg)

**Vanguard** adalah boilerplate full-stack modern yang dirancang untuk mempercepat pengembangan aplikasi web yang kuat dan aman. Mengintegrasikan backend berperforma tinggi dengan Go (framework Gin, ORM GORM, logging Zerolog) dan frontend interaktif menggunakan React (dengan compiler SWC, dukungan TypeScript, dan build tool Vite), serta dilengkapi dengan implementasi Role-Based Access Control (RBAC) untuk manajemen otorisasi yang fleksibel.

## Fitur Utama

* **Backend (Go):**
    * **[Gin](https://gin-gonic.com/)**: Framework web minimalis dengan performa tinggi.
    * **[GORM](https://gorm.io/)**: ORM yang fantastis untuk kemudahan interaksi dengan database.
    * **[Zerolog](https://github.com/rs/zerolog)**: Logging yang efisien dan terstruktur.
    * Struktur proyek yang terorganisir dengan baik.
    * Contoh konfigurasi database.
    * Middleware umum (misalnya, CORS).
* **Frontend (React):**
    * **[React](https://react.dev/)**: Library JavaScript populer untuk membangun antarmuka pengguna.
    * **[TypeScript](https://www.typescriptlang.org/)**: Superset JavaScript yang menambahkan static typing untuk meningkatkan keamanan dan maintainability kode.
    * **[Vite](https://vitejs.dev/)**: Build tool generasi berikutnya yang sangat cepat untuk pengembangan frontend.
    * **[SWC](https://swc.rs/)**: Compiler super cepat untuk TypeScript dan JavaScript.
    * Struktur folder yang skalabel.
    * Contoh komponen UI dasar.
    * Konfigurasi dasar untuk routing dan state management (dapat diintegrasikan sesuai kebutuhan proyek).
* **Role-Based Access Control (RBAC):**
    * Implementasi dasar RBAC untuk mengelola hak akses pengguna berdasarkan peran.
    * Contoh definisi peran dan izin.
    * Middleware untuk melindungi rute backend berdasarkan peran.
* **Konfigurasi:**
    * Manajemen konfigurasi yang mudah melalui file `.env` atau mekanisme serupa.
* **Pengembangan:**
    * Skrip untuk menjalankan backend dan frontend secara terpisah atau bersamaan.
    * Hot module replacement (HMR) untuk pengembangan frontend yang cepat.

## Cara Memulai

Ikuti langkah-langkah di bawah ini untuk menyiapkan dan menjalankan boilerplate Vanguard di lingkungan pengembangan Anda.

### Prasyarat

Pastikan Anda telah menginstal alat berikut di sistem Anda:

* **[Go](https://go.dev/dl/) (versi 1.20 atau lebih tinggi)**
* **[Node.js](https://nodejs.org/) (versi 18 atau lebih tinggi)**
* **[npm](https://www.npmjs.com/) atau [yarn](https://yarnpkg.com/)**
* **[Docker](https://www.docker.com/)** (opsional, untuk deployment containerized)
* **Database** (misalnya, PostgreSQL, MySQL) yang ingin Anda gunakan (konfigurasi akan dilakukan nanti).

### Langkah-langkah Instalasi

1.  **Clone Repository:**
    ```bash
    git clone <URL_REPOSITORY_ANDA>
    cd vanguard
    ```

2.  **Konfigurasi Backend:**
    * Navigasi ke direktori `backend`:
        ```bash
        cd backend
        ```
    * Salin file contoh konfigurasi:
        ```bash
        cp .env.example .env
        ```
    * Edit file `.env` dan sesuaikan dengan konfigurasi database Anda (misalnya, nama database, username, password).
    * Install dependencies Go:
        ```bash
        go mod tidy
        ```

3.  **Konfigurasi Frontend:**
    * Kembali ke direktori root proyek:
        ```bash
        cd ../frontend
        ```
    * Install dependencies frontend menggunakan npm atau yarn:
        ```bash
        npm install
        # atau
        yarn install
        ```
    * Salin file contoh konfigurasi (jika ada):
        ```bash
        cp .env.example .env
        ```
    * Edit file `.env` di direktori `frontend` jika diperlukan (misalnya, untuk konfigurasi API backend).

### Menjalankan Aplikasi

Anda dapat menjalankan backend dan frontend secara terpisah atau bersamaan.

#### Menjalankan Backend

Dari direktori `backend`:

```bash
go run main.go
