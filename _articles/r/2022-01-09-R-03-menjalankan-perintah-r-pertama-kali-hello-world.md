---
title: "R: 03 Menjalankan Perintah R Pertama Kali, “Hello World!”"
categories: R
tags: R
---
<p align="center">
  <img src="/assets/images/r-proglang/r-logo.png" alt="Logo R" title="Logo R" class="logo-topic" />
</p>

Sudah menjadi ritual wajib setelah instalasi bahasa pemrograman adalah dengan menjalankan program bernama “Hello World!” bagi yang baru belajar pemrograman dan artikel ini adalah yang pertama digunakan sebagai referensi tidak perlu khawatir, “Hello World!” hanyalah program untuk memunculkan kata tersebut menggunakan perintah bahasa pemrograman, contohnya akan dipraktikkan menggunakan bahasa R.  

Buka terminal (ctrl + alt + t) dan ketikkan perintah 
{% highlight bash %}
R
{% endhighlight %}

<p align="center">
  <img src="/assets/images/r-proglang/r-03-membuka-r-prompt.png" alt="R Prompt" title="R Prompt"/>
</p>

Maka kita telah masuk ke R prompt, di sini kita bisa mengetikkan perintah dalam bahasa R. Sebagai contoh kita masukkan perintah di bawah ini.

{% highlight r %}
print("Hello World!")
{% endhighlight %}

<p align="center">
  <img src="/assets/images/r-proglang/r-03-hello-world.png" alt="R Hello World" title="R Hello World"/>
</p>

Hasilnya akan keluar seperti gambar di atas, selamat kamu sudah membuat program pertama "Hello World!" dengan menggunakan bahasa R. Untuk keluar dari prompt, kita dapat mengetikkan perintah `q()` lalu tekan `y` untuk keluar.

<p align="center">
  <img src="/assets/images/r-proglang/r-03-quit-r-prompt.png" alt="R Quit R Prompt" title="R Quit R Prompt"/>
</p>

Sedikit penjelasan dari kalimat `Save workspace image?` adalah apakah kita ingin menyimpan history dari apa yang telah kita tuliskan menggunakan prompt sebelumnya atau tidak. 

Workspace image tersebut (pada ubuntu) tersimpan pada file `.Rhistory` di directory tempat kita membuka terminal prompt tadi. File `.Rhistory` bersifat tersembunyi atau hidden, untuk melihatnya bisa menggunakan perintah `ctrl+h`.

<p align="center">
  <img src="/assets/images/r-proglang/r-03-rhistory-path.png" alt="R History Path" title="R History Path"/>
</p>

<p align="center">
  <img src="/assets/images/r-proglang/r-03-rhistory-open.png" alt="R History Open File" title="R History Open File"/>
</p>

Sekian artikel kali ini, semoga bermanfaat dan selamat mencoba.

