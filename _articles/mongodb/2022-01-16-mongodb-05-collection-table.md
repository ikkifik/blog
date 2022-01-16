---
title: "MongoDB: 05 Collection == Table?"
categories: MongoDB
tags: MongoDB
---
<p align="center">
  <img src="/assets/images/mongodb/mongodb-logo.png" alt="Logo MongoDB" class="logo-topic" title="Logo MongoDB" />
</p>

Dalam istilah mongodb, bagi yang pernah belajar database relasional seperti MySQL, collection dapat dianalogikan sebagai tabel. Cara membuat collection di mongodb langsung dengan menambahkan atau menyisipkan (insert) data, perintahnya sebagai berikut,  

{% highlight bash %}
use toko

db.produk1.insertOne({
    "nama": "Kopi Cappuchino",
    "harga": 22000
})
{% endhighlight %}

Pastikan sedang berada di database yang akan kita buat, pada artikel saya sebelumnya saya ingin membuat database bernama `toko` namun pada mongodb database baru akan terbuat ketika data pertama kali ditambahkan.

<p align="center">
  <img src="/assets/images/mongodb/mongodb-05-menambahkan-data.png" alt="MongoDB menambahkan data" title="MongoDB menambahkan data" />
</p>

Pada gambar di atas saya telah berhasil membuat sebuah database, sebuah collection, sekaligus menambahkan sebuah data. Sebagai bukti telah ada database baru bernama `toko` bisa dicek dengan menggunakan perintah `show dbs`.

<p align="center">
  <img src="/assets/images/mongodb/mongodb-05-cek-database-yang-digunakan-sudah-terbuat.png" alt="MongoDB cek database yang digunakan sudah terbuat" title="MongoDB cek database yang digunakan sudah terbuat" />
</p>

Sedangkan untuk melihat data yang telah ditambahkan dapat menggunakan perintah `db.<nama_collection>.find()`, sebagai contoh saya akan menampilkan data pada collection `produk1`.

{% highlight bash %}
db.produk1.find()
{% endhighlight %}

<p align="center">
  <img src="/assets/images/mongodb/mongodb-05-menampilkan-data-pada-collection.png" alt="MongoDB menampilkan data pada collection" title="MongoDB membuat database" />
</p>

Berhasil! Pada artikel selanjutnya saya akan membahas lebih banyak tentang cara menyisipkan data (_insert_).

