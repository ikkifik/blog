---
title: "R: 04 Variabel pada R"
categories: R
tags: R
---
<p align="center">
  <img src="/assets/images/r-proglang/r-logo.png" alt="Logo R" />
</p>

Variabel digunakan sebagai wadah penyimpanan data yang nilainya dapat diubah sesuai kebutuhan. Pada R variabel dapat dituliskan dalam beberapa aturan, antara lain:
  - Menggunakan huruf, angka, garis bawah/underscore, dan titik  
    `var1, var2, var_1, var.1, var2.`
  - Dapat diawali titik, tapi setelah titik tidak bisa dibersamai angka  
    `.variabel`
  - Tidak bisa diawali garis bawah/underscore dan angka  

Deklarasi variabel dapat dilakukan dengan menggunakan simbol `"<-"` atau `"="` seperti berikut:
{% highlight r %}
var.1 <- "Hello World!"
var.2 = "Zuhdi Fikri"
{% endhighlight %}

<p align="center">
  <img src="/assets/images/r-proglang/r-04-deklarasi-variabel.png" alt="deklarasi variabel pada R" title="deklarasi variabel pada R" />
</p>

Melihat variabel yang tersedia atau yang telah dideklarasikan dapat digunakan fungsi `ls()`

<p align="center">
  <img src="/assets/images/r-proglang/r-04-daftar-variabel-yang-telah-dideklarasikan.png" alt="ls() melihat daftar variabel yang tersedia" title="ls() melihat daftar variabel yang tersedia" />
</p>


Pada R variabel dapat dihapus menggunakan fungsi `rm(nama_variabel)`

<p align="center">
  <img src="/assets/images/r-proglang/r-04-menghapus-variabel.png" alt="rm(nama_variabel) untuk menghapus variabel" title="rm(nama_variabel) untuk menghapus variabel" />
</p>

Sekian artikel kali ini, selamat mencoba dan semoga bermanfaat.