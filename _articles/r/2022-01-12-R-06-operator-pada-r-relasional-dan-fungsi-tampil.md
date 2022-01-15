---
title: "R: 06 Operator pada R (Relasional) dan fungsi tampil cat()"
categories: R
tags: R
---
<p align="center">
  <img src="/assets/images/r-proglang/r-logo.png" alt="Logo R" title="Logo R" class="logo-topic" />
</p>

Sebelum memulai praktik operator relasional, saya akan mengenalkan fungsi lain yang dapat digunakan sebagai keluaran (output) selain fungsi print() yaitu cat().  

Apa bedanya? Fungsi print() akan menampilkan keluaran dalam bentuk vector, sedangkan cat() akan menampilkan keluaran dalam bentuk konten. Fungsi cat() sangat berguna ketika kita ingin menampilkan gabungan 2 kata atau lebih.

<p align="center">
  <img src="/assets/images/r-proglang/r-06-perbedaan-fungsi-print-cat.png" alt="Perbedaan fungsi print() dan cat()" title="Perbedaan fungsi print() dan cat()" />
</p>

Fungsi print() juga dapat menampilkan gabungan kata, hanya saja membutuhkan sebuah fungsi lain bernama paste().

<p align="center">
  <img src="/assets/images/r-proglang/r-06-penggunaan-fungsi-print-dengan-paste.png" alt="Penggunaan fungsi print() dengan paste()" title="Penggunaan fungsi print() dengan paste()" />
</p>

----
**Operator Relasional atau Pembanding**

Bagi yang pernah bersekolah di jenjang Sekolah Dasar (SD) pasti sudah tidak asing lagi dengan operator relasional atau operator pembanding. Operator yang membandingkan antara satu nilai dengan nilai yang lain dengan hasil berupa pernyataan benar `(TRUE)` atau salah `(False)`.

    <   : kurang dari
    >   : lebih dari
    <=  : kurang dari sama dengan
    >=  : lebih dari sama dengan
    ==  : sama dengan
    !=  : tidak sama dengan

Berikut hasil praktik penerapan operator relasional atau pembanding pada R juga penggunaan fungsi cat() untuk menampilkan hasilnya.

<p align="center">
  <img src="/assets/images/r-proglang/r-06-operator-relasional.png" alt="Praktik operator relasional R" title="Praktik operator relasional R" />
</p>