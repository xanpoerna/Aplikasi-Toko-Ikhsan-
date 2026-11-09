# Aplikasi Toko

Aplikasi Toko merupakan aplikasi desktop berbasis Java yang dikembangkan menggunakan JavaFX untuk membangun Graphical User Interface (GUI). Aplikasi ini dibuat untuk mengelola data produk toko berdasarkan kode produk, nama produk, kategori, dan harga yang dimasukkan oleh pengguna.

Aplikasi ini memiliki tiga halaman, yaitu Daftar Produk, Form Tambah Produk, dan Detail Produk agar mudah digunakan oleh pengguna.

## Fitur

- Input kode produk.
- Input nama produk.
- Pilihan kategori produk (Makanan dan Minuman).
- Input harga produk.
- Menampilkan daftar produk dalam bentuk tabel.
- Pencarian produk berdasarkan nama produk.
- Menampilkan detail produk yang dipilih.
- Menampilkan harga dalam format Rupiah.
- Validasi input untuk memastikan data yang dimasukkan sesuai.
- Pencegahan kode produk yang sama.

## Teknologi yang Digunakan

- Java JDK 17
- JavaFX 21
- Apache Maven
- Apache NetBeans IDE
- JavaFX Scene Builder
- FXML

## Tampilan Aplikasi
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ea589335-112e-498e-a37e-96551b953143" />


## Aturan Validasi

| Input | Aturan |
|---|---|
| Kode produk | Wajib diisi dan tidak boleh sama dengan kode produk lain |
| Nama produk | Tidak boleh kosong |
| Harga | Harus berupa angka dan lebih dari nol |

## Struktur Project

```
aplikasiToko/
├── src/
│   └── main/
│       ├── java/
│       │   └── kelas/
│       │       ├── Navigator.java
│       │       ├── controller/
│       │       │   ├── DaftarController.java
│       │       │   ├── DetailController.java
│       │       │   └── FormController.java
│       │       ├── data/
│       │       │   └── DataProduk.java
│       │       └── model/
│       │           └── Produk.java
│       └── resources/
│           └── fxml/
│               ├── DaftarView.fxml
│               ├── DetailView.fxml
│               └── FormView.fxml
├── pom.xml
└── README.md
```

## Cara Menjalankan

### 1. Clone Repository

Buka terminal atau Command Prompt, kemudian jalankan:

```
git clone https://github.com/nizaraffan/AplikasiToko
```

### 2. Masuk ke Direktori Project

```
cd aplikasiToko
```

### 3. Periksa Instalasi Java dan Maven

Pastikan Java dan Maven sudah terpasang:

```
java -version
mvn -version
```

### 4. Buka Project

Buka Apache NetBeans, kemudian pilih File → Open Project. Cari folder project aplikasiToko.

### 5. Jalankan Aplikasi

Buka terminal pada direktori utama project, kemudian jalankan:

```
mvn javafx:run
```

Tunggu hingga proses build selesai. Jika berhasil, aplikasi Toko akan terbuka.

## Cara Menggunakan Aplikasi

1. Jalankan aplikasi Toko.
2. Klik tombol Tambah pada halaman Daftar Produk.
3. Masukkan kode produk dan nama produk.
4. Pilih kategori produk.
5. Masukkan harga produk.
6. Klik tombol Simpan.
7. Detail produk akan ditampilkan pada halaman Detail.
8. Kembali ke Daftar Produk untuk melihat semua produk.
9. Ketik nama produk pada kolom pencarian untuk mencari produk.
10. Pilih produk pada tabel, lalu klik tombol Detail untuk melihat informasinya.

## Struktur Program

Program ini menggunakan konsep pemisahan fungsi berdasarkan package:

- **Model:** Produk.java digunakan untuk menyimpan data produk dan memeriksa kebenaran datanya.
- **Data:** DataProduk.java digunakan untuk menyimpan daftar produk dan mencegah kode produk yang sama.
- **Controller:** DaftarController.java, FormController.java, dan DetailController.java digunakan untuk mengatur interaksi antara pengguna dan tampilan aplikasi.
- **Navigator:** Navigator.java digunakan untuk mengatur perpindahan antar halaman.
- **FXML:** DaftarView.fxml, FormView.fxml, dan DetailView.fxml digunakan untuk membangun tampilan antarmuka aplikasi.
