---
title: "Redis: 02 Instalasi Redis di Linux Ubuntu"
categories: "Redis"
tags: "Redis"
---

<p align="center">
  <img src="/assets/images/redis/redis-logo.png" alt="Logo Redis" title="Logo Redis" class="logo-topic" />
</p>

Setelah mengenal sekilas tentang apa itu redis dan konsep databasenya, sekarang kita akan coba install redis di Ubuntu 20.04 melalui Ubuntu official PPA menggunakan apt. Buka terminal dengan `ctrl + alt + t` ikuti langkah di bawah ini.

Tambahkan repository redis

	sudo add-apt-repository ppa:redislabs/redis

Lalu update repository, walaupun untuk versi ubuntu setelah 18.04 sudah tidak perlu karena setelah menambahkan repository ubuntu akan langsung otomatis melakukan update.

	sudo apt update

Install redis
	
	sudo apt install redis

Cek apakah redis sudah berhasil terpasang atau belum dengan perintah `redis-cli --version`.  

<p align="center">
  <img src="/assets/images/redis/redis-02-version-check.png" alt="Cek Versi Redis" title="Cek Versi Redis" />
</p>

Cek juga koneksi antara redis client dengan redis server dengan mengetikan `ping`, bila ada feedback `PONG` berarti redis client telah terhubung dengan redis server.  

<p align="center">
  <img src="/assets/images/redis/redis-02-connection-check.png" alt="Cek Koneksi Redis Client dengan Redis Server" title="Cek Koneksi Redis Client dengan Redis Server" />
</p>

----

Apabila ketika masuk ke interface redis-cli ternyata tampilannya seperti ini  

<p align="center">
  <img src="/assets/images/redis/redis-02-connection-refused.png" alt="Redis Server Connection Refused" title="Redis Server Connection Refused" />
</p>

Aktifkan terlebih dahulu service redis-server dengan perintah `sudo systemctl start redis-server`, untuk mengecek statusnya bisa dengan perintah `sudo systemctl status redis-server`, jika statusnya running berarti redis-server telah berhasil aktif.

<p align="center">
  <img src="/assets/images/redis/redis-02-activate-redis-server.png" alt="Aktivasi Service Redis Server" title="Aktivasi Service Redis Server" />
</p>