# Swagger Petstore API Testing - QA



Selamat datang di repositori API Testing saya!

Proyek ini adalah dokumentasi pengujian API (Application Programming Interface) secara komprehensif menggunakan **Swagger Petstore** sebagai sistem **dummy.** 



Tujuan utama dari proyek ini adalah untuk mendemonstrasikan pemahaman saya mengenai alur kerja Quality Assurance (QA) secara end-to-end—mulai dari membaca API Contract, menyusun skenario Test Case, mengeksekusi pengujian via Postman, hingga menyusun Bug Report yang profesional.



## Tools \& Technologies

- API Testing: Postman

- API Documentation: Swagger / OpenAPI

- Test Management \& Reporting: Microsoft Excel

- Testing Methodology: Black-box Testing, Positive \& Negative Testing, Security Edge-cases (XSS Injection test).



---


## 📁 Project Structure

Repositori ini disusun agar mudah dibaca dan dipahami alurnya:



```text

├── 📁 Contract/

│   └── api contract petstore.json              # Blueprint/API Contract asli sebagai acuan testing.

├── 📁 Postman-Files/

│   ├── Swagger Petstore.postman\_collection.json  # File kumpulan request \& automation test.

│   └── pet store swagger.postman\_environment.json # File environment variables (Base URL, dll).

└── 📁 Reports/

&#x20;   ├── Swagger\_Petstore\_Complete\_TestCases\_Final.xlsx  # Dokumen berisi ratusan skenario test cases.

&#x20;   └── QA\_Bug\_Report\_Petstore.xlsx                     # Laporan celah/bug sistem (High, Medium, Low severity).


---


## Testing Scope & Key Findings
Pengujian difokuskan pada validasi struktur data, keamanan input, dan respon logika bisnis pada endpoint utama (Pet, User, dan Store).

Highlight Temuan Bug (Bug Report):
Sistem yang baik tidak hanya diuji fungsi normalnya (Positive), tapi juga harus tahan terhadap kesalahan (Negative). Berikut beberapa bug menarik yang berhasil saya temukan dan laporkan:

🔴 [High Severity]: Fatal error (500 Internal Server Error) saat mencoba membuat user dengan input array/list yang dimanipulasi, yang bisa berpotensi merusak service.

🟠 [Medium Severity]: Validasi lemah pada endpoint form-data. Sistem mengembalikan status 200 OK dan menyimpan data kosong meskipun mandatory fields (seperti nama pet) tidak diisi.

🟡 [Low Severity]: Response code yang kurang sesuai standar RESTful, seperti sistem memberikan 404 Not Found alih-alih 400 Bad Request saat diserang dengan format tipe data ID yang salah.


## How to Run the Tests (Postman)

Ingin mencoba menjalankan test script ini sendiri? Gampang banget:

- Clone atau download repositori ini.

- Buka aplikasi Postman.

- Klik tombol Import, lalu pilih file koleksi (.postman_collection.json) dan environment (.postman_environment.json) dari folder Postman-Files.

- Jangan lupa aktifkan environment pet store swagger di pojok kanan atas Postman.

- Jalankan melalui Collection Runner untuk melihat hasil eksekusi test case secara langsung!

