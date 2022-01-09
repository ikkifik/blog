---
title: "R: 02 Instalasi R di Linux Ubuntu"
categories: R
tags: R
---
<p align="center">
  <img src="/assets/images/r-proglang/r-logo.png" alt="Logo R" />
</p>

Artikel kali ini saya akan bagikan cara instalasi bahasa R di linux ubuntu, mengambil referensi dari dokumentasi bahasa R di [cloud.r-project.org](https://cloud.r-project.org/) perintah berikut dapat dilakukan melalui terminal linux (Ctrl + Alt + T).  

Untuk mengeksekusi perintah di bawah dapat dilakukan melalui login root atau gunakan sudo di awal perintah, saya sendiri lebih suka menggunakan sudo ketimbang masuk sepenuhnya sebagai root untuk menghindari masalah karena privillege selama instalasi atau ketika menggunakan nantinya.  

Langkah pertama lakukan update packages dari ubuntu  

{% highlight bash %}
sudo apt update
{% endhighlight %}

Selanjutnya install 2 packages helper yang dibutuhkan

{% highlight bash %}
sudo apt install --no-install-recommends \
software-properties-common dirmngr
{% endhighlight %}

Tambahkan signing key sebelum menambahkan repository, untuk memastikan kebenaran repository yang kita pasang.

{% highlight bash %}
wget -qO- \ 
https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc | \ 
sudo tee -a /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc
{% endhighlight %}

Tambahkan repository R versi 4.0 dari CRAN 
{% highlight bash %}
sudo add-apt-repository \ 
"deb https://cloud.r-project.org/bin/linux/ubuntu $(lsb_release -cs)-cran40/"
{% endhighlight %}

Terakhir, install R berikut dependency nya
{% highlight bash %}
sudo apt install --no-install-recommends r-base
{% endhighlight %}

Sebagai tambahan, dapat diinstall juga repository c2d4u yang berfungsi sebagai precompiled R package untuk pengguna Ubuntu.
{% highlight bash %}
sudo add-apt-repository ppa:c2d4u.team/c2d4u4.0+
{% endhighlight %}

Jika proses instalasi di atas telah selesai dan berhasil, dapat kita cek versi R dengan perintah 
{% highlight bash %}
R --version
{% endhighlight %}

<p align="center">
  <img src="/assets/images/r-proglang/r-02-instalasi-r-di-linux-ubuntu.png" alt="R Version" />
</p>

Jika telah tampil seperti gambar di atas, berarti instalasi R telah berhasil, selamat!