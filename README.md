# My First API (Go Backend)

Ini adalah proyek RESTful API sederhana yang dibangun menggunakan bahasa pemrograman Go (Golang). Proyek ini dibuat untuk mempelajari dasar-dasar backend HTTP routing (Go 1.22+), penanganan JSON, validasi input, dan memunculkan dokumentasi otomatis menggunakan Swagger.

## 🚀 Fitur
* **Mendapatkan daftar buku** (GET)
* **Menambahkan buku baru** (POST) dengan validasi input
* **Dokumentasi API interaktif** menggunakan Swagger UI

## 🛠️ Prasyarat
* [Go](https://go.dev/dl/) versi 1.22 atau versi lebih baru (karena menggunakan standard HTTP routing method terbaru `GET /`, `POST /`).

## 📦 Instalasi & Cara Menjalankan

1. Buka terminal dan arahkan ke folder proyek ini:
   ```bash
   cd my-first-api
   ```

2. Pastikan semua *module* / *library* (seperti validator & swagger) sudah terunduh:
   ```bash
   go mod tidy
   ```

3. Jalankan server:
   ```bash
   go run main.go
   ```

   Server akan berjalan di `http://localhost:8080`.

## 📚 Endpoint API

Berikut adalah beberapa Endpoint yang bisa diakses:

### 1. Mendapatkan Semua Buku
* **Method:** `GET`
* **URL:** `http://localhost:8080/books`
* **Contoh Request (Windows / PowerShell):**
  ```bash
  curl.exe http://localhost:8080/books
  ```

### 2. Menambahkan Buku Baru
* **Method:** `POST`
* **URL:** `http://localhost:8080/books`
* **Headers:** `Content-Type: application/json`
* **Body:**
  ```json
  {
    "title": "Buku Baru",
    "author": "Penulis Baru"
  }
  ```
* **Contoh Request (Windows / PowerShell):**
  ```bash
  Invoke-RestMethod -Method Post -Uri "http://localhost:8080/books" -ContentType "application/json" -Body '{"title": "Buku Baru", "author": "Penulis Baru"}'
  ```

## 📖 Dokumentasi Swagger UI
API ini juga dilengkapi dengan dokumentasi interaktif dari antarmuka Swagger.

Saat server sedang menyala, cukup buka alamat berikut di web browser kamu:
👉 **[http://localhost:8080/swagger/](http://localhost:8080/swagger/)**

*(Jika kamu mengubah kode API, jangan lupa untuk menjalankan perintah `swag init` di terminal agar dokumentasinya ter-update).*
