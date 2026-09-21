# SISTEM MANAJEMEN DATA PRODUK KOPI

## Deskripsi
Aplikasi web sederhana berbasis PHP untuk menyimpan, mengolah, dan menampilkan data produk kopi dengan konsep 3 Layer Architecture.

## Struktur
```text
sistem-manajemen-kopi/
├── products.php
├── functions.php
├── index.php
└── README.md
```

### Data Layer — products.php
Menyimpan data produk kopi dalam multidimensional array:
ID, nama, kategori, harga, stok, dan deskripsi.

### Processing Layer — functions.php
Mengolah data menggunakan:
- `hitungTotalNilaiStok()` untuk menghitung nilai aset stok.
- `formatRupiah()` untuk format harga.
- `stokKritis()` untuk mengecek stok kurang dari 3.

### Presentation Layer — index.php
Menggunakan `require_once` untuk memanggil file lain, kemudian menampilkan data menggunakan `foreach` ke tabel HTML.

## Produk Contoh
- Kopi Gayo Arabika
- Kopi Robusta Aceh
- Kopi Arabika Toraja
- Kopi Liberika
- Kopi Susu Gula Aren

## Rumus
```text
Nilai Stok = Harga × Stok
Total Aset = Σ(Harga × Stok)
```

## Stok Kritis
Jika `stok < 3`, baris produk diberi tanda khusus sebagai **KRITIS**.

## Cara Menjalankan
1. Instal XAMPP.
2. Jalankan Apache.
3. Salin folder project ke `C:\xampp\htdocs\`.
4. Buka:
```text
http://localhost/sistem-manajemen-kopi/
```

## Teknologi
PHP, HTML, CSS, XAMPP, Apache.

## Tujuan Pembelajaran
Memahami pemisahan Data Layer, Processing Layer, dan Presentation Layer serta penggunaan array, function, conditional, `foreach`, dan `require_once` pada PHP.

## Pengembangan
Sistem dapat dikembangkan dengan MySQL, login admin, CRUD produk, pencarian, filter kategori, transaksi, dashboard, dan laporan stok.
