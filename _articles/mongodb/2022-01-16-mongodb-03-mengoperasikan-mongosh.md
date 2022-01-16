---
title: "MongoDB: 03 Mengoperasikan mongodb pertama kali - Mongosh"
categories: MongoDB
tags: MongoDB
---
<p align="center">
  <img src="/assets/images/mongodb/mongodb-logo.png" alt="Logo MongoDB" class="logo-topic" title="Logo MongoDB" />
</p>

Untuk mengoperasikan mongodb kita dapat gunakan mongodb shell atau dikenal dengan `mongosh`. `Mongosh` secara singkat adalah environment yang dibangun menggunakan javascript dan node.js untuk berinteraksi dengan mongodb, kita bisa gunakan mongosh untuk melakukan operasi dan query pada mongodb.  

`Mongosh` juga sudah tersedia bersamaan dengan instalasi mongodb. Cara mengaktifkan `mongosh` hanya dengan mengetikkan kata `mongosh` di terminal.  

{% highlight bash %}
Mongosh
{% endhighlight %}

<p align="center">
  <img src="/assets/images/mongodb/mongodb-03-mengoperasikan-mongosh.png" alt="Mengoperasikan Mongosh" title="Mengoperasikan Mongosh" />
</p>

Apabila pembaca menemukan di beberapa sumber yang menggunakan perintah `mongo` untuk berinteraksi dengan mongodb melalui terminal seperti gambar di bawah.  

<p align="center">
  <img src="/assets/images/mongodb/mongodb-03-mengoperasikan-mongo.png" alt="Mengoperasikan Mongo" title="Mengoperasikan Mongo" />
</p>

`Mongo` dan `Mongosh` pada intinya sama saja, sama-sama bisa digunakan untuk berinteraksi dengan database mongodb dan melakukan operasi di dalamnya.  

Melalui dokumentasi mongodb di [docs.mongodb.com](https://docs.mongodb.com/mongodb-shell/#mongodb-binary-bin.mongosh), mongosh (mongo shell) adalah versi terbaru dari mongo yang menawarkan fitur yang lebih baik, seperti:  
  - Syntax highlighting;  
  - Command history; dan  
  - Logging.  

Pada artikel selanjutnya saya akan membawakan pembahasan menggunakan mongosh.  