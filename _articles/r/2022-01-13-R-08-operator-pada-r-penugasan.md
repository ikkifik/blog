---
title: "R: 08 Operator pada R (Penugasan)"
categories: R
tags: R
---
<p align="center">
  <img src="/assets/images/r-proglang/r-logo.png" alt="Logo R" />
</p>

Sebenarnya operator penugasan telah kita ketahui dari artikel sebelumnya. Operator penugasan atau sering dikenal dengan istilah _assignment operator_ digunakan untuk memberikan "tugas" (nilai) kepada variabel.  

Pada R, terdapat 2 kelompok operator penugasan yang dibedakan berdasarkan simbol arahnya.

----

**Kiri**  
Operator penugasan dengan arah menghadap ke kiri lebih umum digunakan, terlebih untuk simbol `"="` banyak digunakan oleh berbagai bahasa pemrograman.

    =    
    <-   
    <<-  

<p align="center">
  <img src="/assets/images/r-proglang/r-08-penugasan-kiri.png" alt="Operator penugasan (Kiri) pada R" title="Operator penugasan (Kiri) pada R" />
</p>

----

**Kanan**  
Operator penugasan dengan arah menghadap ke kanan memang dapat digunakan, namun tidak terlalu umum digunakan. 

    ->   
    ->> 

<p align="center">
  <img src="/assets/images/r-proglang/r-08-penugasan-kanan.png" alt="Operator penugasan (Kanan) pada R" title="Operator penugasan (Kanan) pada R" />
</p>

----

Jika kita cari di beberapa forum diskusi yang membahas tentang operator penugasan (assignment) pada R, banyak muncul perdebatan antara operator penugasan satu dengan yang lainnya, mana yang baiknya digunakan disaat A atau disaat B.  

Namun, ada pendapat yang saya juga setuju yaitu dengan menggunakan operator penugasan menghadap ke kiri `(=, <-, <<-)` tapi harus konsisten. Ketika menggunakan simbol sama dengan `("=")` maka seterusnya simbol sama dengan, juga ketika menggunakan simbol panah `("<-")` seterusnya simbol panah.  

Jika menganut preferensi bahasa R, operator penugasan yang populer digunakan adalah panah `("<-")`.