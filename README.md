# Tugas Pendahuluan Modul 5 - Bootstrap

Pemrograman Web - Ganjil 2026/2027

Nama : Satria Ari Permana
NIM  : 103092400056

1. Pengertian Bootstrap
Bootstrap adalah framework front-end open source yang berisi kumpulan CSS dan JavaScript siap pakai untuk membangun tampilan website yang responsif dengan pendekatan mobile-first. Kegunaan Bootstrap antara lain:
- Mempercepat pembuatan antarmuka karena menyediakan komponen siap pakai seperti navbar, card, form, button, dan modal.
- Membuat tampilan website responsif sehingga menyesuaikan ukuran layar HP, tablet, dan desktop melalui sistem grid.
- Menjaga konsistensi tampilan di berbagai browser.
- Mengurangi kebutuhan menulis CSS dari nol karena tersedia banyak class utility.

2. Memasang Bootstrap
Beberapa cara menggunakan Bootstrap pada project:
- **CDN**: menautkan file CSS dengan tag `<link>` dan JS dengan tag `<script>` dari server CDN (misalnya jsDelivr). Cara paling cepat, tetapi membutuhkan koneksi internet.
- **Download langsung**: mengunduh file Bootstrap yang sudah dikompilasi (CSS dan JS), meletakkannya di folder project, lalu menautkannya secara lokal.
- **Package manager**: memasang lewat npm, yarn, atau composer, misalnya `npm install bootstrap@5.3.8`.
- **Source Sass**: memakai file Sass Bootstrap untuk kustomisasi variabel, kemudian dikompilasi sendiri.
Contoh CDN Bootstrap 5.3.8:

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js"></script>
```

3. Grid dan Breakpoint
Grid Bootstrap adalah sistem tata letak berbasis flexbox dengan 12 kolom dalam satu baris. Strukturnya terdiri dari `container` (pembungkus), `row` (baris), dan `col-*` (kolom). Lebar kolom dihitung dari total 12. Contohnya `col-md-6` berarti kolom selebar 6 dari 12 (setengah lebar) mulai layar md ke atas, sedangkan di layar yang lebih kecil kolom tersusun penuh ke bawah.
Breakpoint adalah batas lebar layar tempat tata letak berubah.

| Breakpoint | Class | Lebar layar |
|------------|-------|-------------|
| Extra small | `col-` | < 576px |
| Small | `col-sm-` | ≥ 576px |
| Medium | `col-md-` | ≥ 768px |
| Large | `col-lg-` | ≥ 992px |
| Extra large | `col-xl-` | ≥ 1200px |
| XXL | `col-xxl-` | ≥ 1400px |
Kegunaannya agar satu kode HTML dapat menampilkan tata letak berbeda sesuai ukuran perangkat, sehingga website responsif.

4. Class Bootstrap

| Class | Kegunaan |
|-------|----------|
| `container` | Pembungkus konten dengan lebar responsif dan berada di tengah halaman |
| `row` dan `col-*` | Membuat tata letak grid baris dan kolom |
| `btn btn-primary` | Mengubah elemen menjadi tombol berwarna biru |
| `text-center` | Meratakan teks ke tengah |
| `bg-success` | Memberi warna latar hijau |
| `shadow` | Memberi bayangan pada elemen |
| `d-flex` | Mengaktifkan display flexbox |
| `mt-3` / `p-4` | Mengatur margin atas dan padding |

5. Gambar Responsif
Tambahkan class `img-fluid` pada tag `<img>`. Class ini menerapkan `max-width: 100%` dan `height: auto`, sehingga gambar mengecil mengikuti lebar elemen induknya dan tidak melebihi ukuran aslinya, dengan perbandingan tinggi-lebar tetap terjaga.

```html
<img src="foto.jpg" class="img-fluid" alt="Foto">
```
