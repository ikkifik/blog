---
title: "R: 07 Operator pada R (Logika)"
categories: R
tags: R
---
<p align="center">
  <img src="/assets/images/r-proglang/r-logo.png" alt="Logo R" />
</p>

Untuk pembahasan operator logika saya akan menggunakan bantuan tabel untuk penjelasan terkait aturan logikanya dan hasil dari aturan logika tersebut.  

----

**NOT**  
Operator logika yang pertama adalah "NOT" atau dalam bahasa Indonesia yang berarti "Bukan" atau "Tidak", disimbolkan dengan tanda seru "!" yang dimaksudkan sebagai nilai terbalik atau kebalikan.  

    Jika kondisi bukan benar maka hasilnya salah, 
    Jika kondisi salah maka hasilnya benar.

<p align="center">
  <img src="/assets/images/r-proglang/r-07-not.png" alt="Konsep operator NOT pada R" title="Konsep operator NOT pada R" />
</p>

Berikut jika operator logika "NOT" diterapkan pada R.

<p align="center">
  <img src="/assets/images/r-proglang/r-07-not-implement.png" alt="Implementasi operator NOT pada R" title="Implementasi operator NOT pada R" />
</p>

----

**AND**  
Penjelasan mudah dari operator logika "AND" adalah dengan mengasumsikannya sebagai **perkalian**.  

    Akan menghasilkan nilai benar jika keduanya bernilai benar.

<p align="center">
  <img src="/assets/images/r-proglang/r-07-and.png" alt="Konsep operator AND pada R" title="Konsep operator AND pada R" />
</p>

Pada R, operator logika "AND" menggunakan simbol "&" dengan 2 macam penggunaan.

    &   : Element-wise Logical AND operator
    &&  : Logical AND operator

<p align="center">
  <img src="/assets/images/r-proglang/r-07-and-implement.png" alt="Implementasi operator AND pada R" title="Implementasi operator AND pada R" />
</p>

Operator logika "AND" dengan 1 simbol (&) akan melakukan perbandingan benar atau salah pada kedua vector dan menampilkan masing-masing hasil perbandingannya, tentang vector akan saya bahas di artikel terpisah yang membahas tentang tipe data.  

Sedangkan operator logika "AND" dengan 2 simbol (&&) juga akan membandingkan 2 vector, namun hanya mengambil urutan pertama dari kedua vector yang dibandingkan.  

----

**OR**  
Operator logika "OR" dapat diasumsikan sebagai **penjumlahan**.

    Akan menghasilkan nilai benar jika salah satu atau keduanya bernilai benar.

<p align="center">
  <img src="/assets/images/r-proglang/r-07-or.png" alt="Konsep operator OR pada R" title="Konsep operator OR pada R" />
</p>

Pada R, operator logika "OR" menggunakan simbol " \| " garis lurus atau bisa disebut pipeline dengan 2 macam penggunaan.  

    |   : Element-wise Logical OR operator
    ||  : Logical OR operator

<p align="center">
  <img src="/assets/images/r-proglang/r-07-or-implement.png" alt="Implementasi operator OR pada R" title="Implementasi operator OR pada R" />
</p>

Sama seperti operator logika "AND," operator logika "OR" dengan satu simbol ( \| ) akan membandingkan 2 vector dan menampilkan masing-masing hasil perbandingannya.  

Sedangkan operator logika "OR" dengan dua simbol ( \|\| ) akan membandingkan 2 vector namun hanya menampilkan hasil vector urutan pertama.  