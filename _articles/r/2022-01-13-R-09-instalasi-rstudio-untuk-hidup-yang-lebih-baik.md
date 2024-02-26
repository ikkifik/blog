---
title: "R: 09 Instalasi RStudio untuk hidup yang lebih baik"
categories: R
tags: R
---
<p align="center">
  <img src="/assets/images/r-proglang/r-logo.png" alt="Logo R" title="Logo R" class="logo-topic" />
</p>

Daripada menggunakan terminal atau bisa disebut CLI based, akan lebih baik kita gunakan fasilitas IDE yang telah tersedia untuk R bernama Rstudio. Rstudio dapat diunduh melalui website officialnya langsung rstudio.com, atau agar memudahkan bisa ikuti link berikut ini, [Unduh RStudio](https://www.rstudio.com/products/rstudio/download/#download).  

Pilih opsi unduhan sesuai dengan sistem operasi masing-masing, saya menggunakan sistem operasi Ubuntu 20.04 LTS maka saya pilih Ubuntu 18/Debian 10 dengan format file `.deb`, lihat gambar di bawah.  

<p align="center">
  <img src="/assets/images/r-proglang/r-09-download-rstudio.png" alt="Download RStudio Official" title="Download RStudio Official" />
</p>

Setelah diunduh silakan masuk ke direktori tempat file unduhan, untuk instalasi .deb di Ubuntu bisa gunakan perintah `sudo dpkg -i <nama_package>.deb` seperti contoh di bawah.  

<p align="center">
  <img src="/assets/images/r-proglang/r-09-install-rstudio.png" alt="Install RStudio di Ubuntu" title="Install RStudio di Ubuntu" />
</p>

Jika instalasi terdapat pesan error seperti gambar di atas, kita dapat lakukan perintah `sudo apt -f install`. Pesan error tersebut terjadi ketika kita menginstall package dari file .deb menggunakan dpkg namun sistem operasi belum memiliki package lain yang mendukung package yang kita install, dalam hal ini rstudio.  

<p align="center">
  <img src="/assets/images/r-proglang/r-09-memperbaiki-package-yang-kurang-untuk-rstudio.png" alt="Memperbaiki Package yang dibutuhkan untuk RStudio" title="Memperbaiki Package yang dibutuhkan untuk RStudio" />
</p>

Setelah instalasi package pendukung telah selesai dan berhasil, Rstudio dapat dicek menggunakan launchpad (Ubuntu) dengan mengetikkan “rstudio” yang akan memunculkan ikon Rstudio.  

<p align="center">
  <img src="/assets/images/r-proglang/r-09-membuka-rstudio-melalui-launchpad.png" alt="Membuka RStudio melalui Ubuntu launchpad" title="Membuka RStudio melalui Ubuntu launchpad" />
</p>

Berikut tampilan awal dari Rstudio.  

<p align="center">
  <img src="/assets/images/r-proglang/r-09-tampilan-awal-rstudio-di-ubuntu.png" alt="Tampilan Awal RStudio di Ubuntu" title="Tampilan Awal RStudio di Ubuntu" />
</p>

Selamat, instalasi telah selesai dan bisa digunakan untuk mulai mengeksekusi program dari R. Di artikel selanjutnya saya akan mulai menuliskan artikel pembahasan R menggunakan Rstudio. Sekian artikel kali ini semoga bermanfaat.