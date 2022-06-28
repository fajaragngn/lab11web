| Nama      | Fajar Agung Nugroho |
| ----------- | ----------- |
| NIM     | 312010448       |
| Kelas   | TI.20.A.1        |

## Langkah langkah praktikum 11

## 1. Buat file baru dengan nama header.php
### Instalasi Codeigniter 4
Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara
manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara
manual

• Unduh Codeigniter dari website https://codeigniter.com/download

• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.

• Ubah nama direktory framework-4.x.xx menjadi ci4.

• Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

![img1!](assets/img/1/11.png)

## 2. Menjalankan CLI (Command Line Interface)
Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk
mengakses CLI buka terminal/command prompt.

![img1!](assets/img/2/1.png)

## 3. Mengaktifkan Mode Debugging
Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk
mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program.

![img1!](assets/img/3/1.png)

Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable
CI_ENVIRINMENT menjadi development.

## 4. Membuat Route Baru.
Tambahkan kode berikut di dalam Routes.php

![img1!](assets/img/4/1.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about

![img1!](assets/img/4/2.png)

Ketika diakses akan mucul tampilan error 404 file not found, itu artinya file/page
tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih
dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

## 5. Membuat Controller
Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php
pada direktori Controller kemudian isi kodenya seperti berikut.

![img1!](assets/img/5/1.png)

Selanjutnya refresh Kembali browser, maka akan ditampilkan hasilnya yaitu halaman
sudah dapat diakses.

![img1!](assets/img/5/2.png)

## 6. Auto Routing
Secara default fitur autoroute pada Codeiginiter sudah aktif. Untuk mengubah status
autoroute dapat mengubah nilai variabelnya. Untuk menonaktifkan ubah nilai true
menjadi false.

![img1!](assets/img/5/3.png)

Tambahkan method baru pada Controller Page seperti berikut.

![img1!](assets/img/5/4.png)

Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan alamat: http://localhost:8080/page/tos

![img1!](assets/img/5/5.png)

## 7. Membuat View
Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file
baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi
kodenya seperti berikut.

![img1!](assets/img/6/1.png)

Ubah method about pada class Controller Page menjadi seperti berikut:

![img1!](assets/img/6/2.png)

Kemudian lakukan refresh pada halaman tersebut.

![img1!](assets/img/6/3.png)

## 8. Membuat Layout Web dengan CSS
Buat file css pada direktori public dengan nama style.css (copy file dari praktikum
lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.

![img1!](assets/img/7/1.png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan
footer.php

![img1!](assets/img/7/22.png)

File app/view/template/footer.php

![img1!](assets/img/7/3.png)

Kemudian ubah file app/view/about.php seperti berikut.

![img1!](assets/img/7/4.png)

Selanjutnya refresh tampilan pada alamat http://localhost:8080/about

![img1!](assets/img/7/5.png)

# Lab 11 (Lanjutan)

## 1. Membuat Database: Studi Kasus Data Artikel

![img1!](assets/img/11/1.png)

## 2. Konfigurasi koneksi database
Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server.

![img1!](assets/img/11/2.png)

## 3. Membuat Model
Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori app/Models dengan nama ArtikelModel.php

![img1!](assets/img/11/3.png)

## 4. Membuat Controller
Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers.

![img1!](assets/img/11/4.png)

## 5. Membuat View
Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file baru dengan nama index.php.

![img1!](assets/img/11/5.png)

Selanjutnya buka browser kembali, dengan mengakses url http://localhost:8080/artikel

![img1!](assets/img/11/6.png)

Belum ada data yang diampilkan. Kemudian coba tambahkan beberapa data pada database agar dapat ditampilkan datanya.

![img1!](assets/img/11/7.png)

Refresh kembali browser, sehingga akan ditampilkan hasilnya.

![img1!](assets/img/11/8.png)

## 6. Membuat Tampilan Detail Artikel
Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. Tambahkan fungsi baru pada Controller Artikel dengan nama view().

![img1!](assets/img/11/9.png)

## Membuat View Detail
Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php.

![img1!](assets/img/11/10.png)