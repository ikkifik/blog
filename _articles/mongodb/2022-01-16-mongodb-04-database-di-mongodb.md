---
title: "MongoDB: 04 Database di MongoDB"
categories: MongoDB
tags: MongoDB
---
<p align="center">
  <img src="/assets/images/mongodb/mongodb-logo.png" alt="Logo MongoDB" class="logo-topic" title="Logo MongoDB" />
</p>

Pada artikel ini saya akan mulai membahas cara pengoperasian dari mongodb menggunakan `mongosh`, dimulai dari bagaimana cara mengoperasikan database dan tabel. Untuk mengecek ketersediaan database pada mongodb dapat dilakukan dengan perintah `show databases` atau singkatnya bisa ditulis `show dbs`.  

{% highlight bash %}
show databases
{% endhighlight %}

<p align="center">
  <img src="/assets/images/mongodb/mongodb-04-show-database.png" alt="MongoDB show database" title="MongoDB show database" />
</p>

Untuk membuat database pada mongodb cukup gunakan `use <nama_database>` sebagai contoh,

{% highlight bash %}
use toko
{% endhighlight %}

<p align="center">
  <img src="/assets/images/mongodb/mongodb-04-membuat-database.png" alt="MongoDB membuat database" title="MongoDB membuat database" />
</p>

Sedangkan untuk mengecek database apa yang kita gunakan sekarang dengan perintah db, walaupun pada mongosh nama database yang saat ini sedang digunakan sudah tertera dengan berubahnya kata `test` menjadi `toko` pada gambar di atas.

{% highlight bash %}
db
{% endhighlight %}

<p align="center">
  <img src="/assets/images/mongodb/mongodb-04-cek-database-yang-digunakan.png" alt="MongoDB cek database yang digunakan" title="MongoDB cek database yang digunakan" />
</p>

Sebenarnya database belum benar-benar dibuat jika hanya menggunakan perintah `use <nama_database>`, database pada mongodb baru akan dibuat setelah kita pertama kali menyimpan data pada database tersebut.

<p align="center">
  <img src="/assets/images/mongodb/mongodb-04-cek-database-yang-digunakan-belum-terbuat.png" alt="MongoDB cek database yang digunakan belum terbuat" title="MongoDB cek database yang digunakan belum terbuat" />
</p>

Pada artikel selanjutnya saya akan membahas mengenai collection yang dengan begitu database yang telah kita `use` sebelumnya dapat terbuat.