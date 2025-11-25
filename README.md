# Proyek Otomasi Tes - Swag Labs (SauceDemo)

Proyek ini adalah contoh kerangka kerja otomasi tes fungsional untuk situs e-commerce [Swag Labs](https://www.saucedemo.com/). Dibangun menggunakan Java, Selenium, dan TestNG, proyek ini bertujuan untuk memverifikasi fungsionalitas utama aplikasi seperti proses login dan manajemen inventaris.

Proyek ini dirancang untuk menunjukkan kompetensi dalam rekayasa jaminan kualitas (Quality Assurance) dengan menerapkan praktik terbaik dalam otomasi tes, mulai dari desain kasus uji hingga eksekusi dan pelaporan.

---

## ✨ Fitur Utama & Sorotan

- **Desain Kasus Uji Terstruktur**: Otomasi didasarkan pada [kasus uji manual](testcase.md) yang terdefinisi dengan baik, mencakup skenario positif dan negatif.
- **Manajemen Dependensi**: Menggunakan **Apache Maven** untuk mengelola semua dependensi proyek secara efisien.
- **Kerangka Kerja Pengujian**: Memanfaatkan **TestNG** untuk menstrukturkan, mengeksekusi, dan mengelola alur tes, termasuk penggunaan anotasi seperti `@Test` dan `@Parameters`.
- **Otomasi Browser**: Menggunakan **Selenium WebDriver** untuk melakukan interaksi nyata pada browser.
- **Konfigurasi Suite Tes**: Alur eksekusi tes dikendalikan melalui file `testng.xml`, yang memungkinkan pengelompokan tes dan pemberian parameter secara eksternal.
- **Pelaporan Tes**: Secara otomatis menghasilkan laporan tes HTML setelah eksekusi menggunakan **Maven Surefire Plugin**.

---

## 🛠️ Tumpukan Teknologi (Tech Stack)

- **Bahasa Pemrograman**: Java 11
- **Alat Otomasi**: Selenium WebDriver 4.27.0
- **Kerangka Kerja Tes**: TestNG 7.10.2
- **Alat Build & Dependensi**: Apache Maven 3.8+
- **Logging**: SLF4J

---

## 📂 Struktur Proyek

```
swaglabs-test/
├── pom.xml                   # File konfigurasi utama Maven
├── testcase.md               # Dokumen kasus uji manual
├── src/
│   ├── main/java/            # (Tidak digunakan secara aktif)
│   └── test/
│       ├── java/
│       │   └── com/juaracoding/swaglabs/
│       │       ├── BaseTest.java       # Kelas dasar untuk setup & teardown browser
│       │       ├── LoginTest.java      # Skrip tes untuk fungsionalitas login
│       │       └── InventoryTest.java  # Skrip tes untuk fungsionalitas inventaris
│       └── resources/
│           └── testng.xml      # Konfigurasi suite tes TestNG
└── target/                     # Direktori output build & laporan tes
```

---

## 🧪 Skenario Tes yang Diotomasi

Proyek ini mengotomatiskan kasus uji yang didefinisikan dalam `testcase.md`.

### Fungsionalitas Login (`LoginTest.java`)
- **TCL-01**: Login berhasil dengan kredensial yang valid.
- **TCL-02**: Login gagal dengan nama pengguna yang tidak valid.
- **TCL-03**: Login gagal dengan kata sandi yang tidak valid.
- **TCL-04**: Login gagal dengan nama pengguna kosong.
- **TCL-05**: Login gagal dengan kata sandi kosong.
- **TCL-06**: Login gagal dengan nama pengguna dan kata sandi kosong.

---

## 🚀 Cara Menjalankan Tes

Untuk menjalankan proyek ini di lingkungan lokal Anda, ikuti langkah-langkah berikut:

### Prasyarat
- **Java Development Kit (JDK)** versi 11 atau lebih tinggi.
- **Apache Maven** terinstal dan terkonfigurasi di sistem Anda.
- **Google Chrome** atau browser lain yang didukung Selenium.

### Langkah-langkah Eksekusi

1.  **Clone Repositori**
    ```bash
    git clone <URL_REPOSITORI_ANDA>
    cd swaglabs-test
    ```

2.  **Jalankan Tes menggunakan Maven**
    Buka terminal atau command prompt di direktori root proyek, lalu jalankan perintah berikut:
    ```bash
    mvn clean test
    ```
    Perintah ini akan secara otomatis mengunduh semua dependensi yang diperlukan, mengompilasi kode, dan menjalankan suite tes yang didefinisikan dalam `src/test/resources/testng.xml`.

---

## 📊 Laporan Tes

Setelah eksekusi selesai, laporan tes akan tersedia di direktori `target/surefire-reports/`.

-   Buka file `index.html` di browser Anda untuk melihat ringkasan hasil tes yang detail dan mudah dibaca.
