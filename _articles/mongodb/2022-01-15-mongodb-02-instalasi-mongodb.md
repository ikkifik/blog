---
title: "MongoDB: Instalasi MongoDB di Linux Ubuntu"
categories: MongoDB
tags: MongoDB
---
<p align="center">
  <img src="/assets/images/mongodb/mongodb-logo.png" alt="Logo MongoDB" class="logo-topic" title="Logo MongoDB" />
</p>

    Bagaimana cara instalasi MongoDB?  

Instalasi pada artikel ini akan menggunakan OS linux Ubuntu versi 20.04 LTS dengan panduan dari website dokumentasinya langsung di [docs.mongodb.com](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/#install-mongodb-community-edition). Di sini saya akan menggunakan MongoDB edisi komunitas yang tentunya saya pilih karena gratis.  

Langkah pertama dengan menambahkan public key agar kita bisa mendapatkan akses repositori instalasi MongoDB. Mari terlebih dahulu buka terminal ubuntu, bisa dengan kombinasi `Ctrl + Alt + T`.  

{% highlight bash %}
wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | \ 
sudo apt-key add -
{% endhighlight %}

<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-menambahkan-public-key-repository-mongodb.png" alt="Public key repository MongoDB" title="Public key repository MongoDB" />
</p>

Public key dianggap berhasil ditambahkan ketika muncul huruf “OK” di terminal. Selanjutnya kita tambahkan repository MongoDB dengan mengetikkan perintah di bawah ini

{% highlight bash %}
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | \ 
sudo tee /etc/apt/sources.list.d/mongodb-org-5.0.list
{% endhighlight %}

<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-menambahkan-repository-mongodb.png" alt="Repository MongoDB" title="Repository MongoDB" />
</p>

Perintah tersebut akan membuat file `.list` pada direktori `/etc/apt/sources.list.d/` dengan nama `mongodb-5.0.list`. Setelah menambahkan repository, saatnya mengupdate repository dengan perintah `apt update`.

{% highlight bash %}
sudo apt update 
{% endhighlight %}

Setelah update repository selesai, kita bisa langsung install mongodb dengan perintah `apt install mongodb-org`.  

{% highlight bash %}
sudo apt-get install -y mongodb-org
{% endhighlight %}

Jika instalasi telah selesai, ketersediaan mongodb dapat kita cek melalui perintah `mongod --version`.  

<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-cek-versi-mongodb.png" alt="Cek versi MongoDB" title="Cek versi MongoDB" />
</p>  

Untuk mengaktifkan mongodb bisa dilakukan dengan mengaktifkan service mongod menggunakan perintah `sudo systemctl start mongod`, lalu kita cek status dari mongodb apakah sudah aktif atau belum dengan perintah `sudo systemctl status mongod`.  

<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-cek-service-mongodb.png" alt="Cek service MongoDB" title="Cek service MongoDB" />
</p>  

----

**Service MongoDB Failed**

Jika setelah instalasi dan ketika kita cek ternyata mongodb gagal aktif dengan tampilan seperti di bawah ini.  

<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-gagal-mengaktifkan-service-mongodb.png" alt="Gagal mengaktifkan service MongoDB" title="Gagal mengaktifkan service MongoDB" />
</p>  

Kendala tersebut bisa saja terjadi karena user permission pada file `.sock` yang mengharuskan kita untuk mengubah kepemilikan file tersebut. Contohnya seperti di bawah ini, 

<!-- https://stackoverflow.com/a/64964015 -->


<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-error-kepemilikan-tmp-sock-mongodb.png" alt="Error kepemilikan file /tmp/mongodb-27017.sock MongoDB" title="Error kepemilikan file /tmp/mongodb-27017.sock MongoDB" />
</p> 

Kepemilikan masih ada di user bernama ikkifik (ikkifik:ikkifik), saya akan ubah kepemilikan file tersebut menjadi mongodb (mongodb:mongodb) dengan perintah,  

{% highlight bash %}
sudo chown -R mongodb:mongodb /var/lib/mongodb
sudo chown mongodb:mongodb /tmp/mongodb-27017.sock
{% endhighlight %}

Setelah diubah menjadi seperti ini,  

<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-solve-error-kepemilikan-tmp-sock-mongodb.png" alt="Memperbaiki error kepemilikan file /tmp/mongodb-27017.sock MongoDB" title="Memperbaiki error kepemilikan file /tmp/mongodb-27017.sock MongoDB" />
</p> 

Sekarang bisa dicoba untuk mengaktifkannya kembali dengan perintah `sudo systemctl start mongod`, lalu kita cek apakah service mongodb telah aktif dengan perintah `sudo systemctl status mongod`.  

<p align="center">
  <img src="/assets/images/mongodb/mongodb-02-cek-service-mongodb.png" alt="Cek service MongoDB" title="Cek service MongoDB" />
</p>  

Service mongodb telah berhasil aktif di mesin (laptop) saya, service mongodb bernama `mongod`.service.  

Perintah `sudo systemctl start mongod` hanya akan mengaktifkan service mongodb selama mesin menyala dan akan kembali mati ketika mesin shutdown, untuk menyalakannya kembali kita perlu menuliskan ulang secara manual perintah `sudo systemctl start mongod`.  

Untuk itu apabila mongodb dibutuhkan untuk selalu aktif setiap kali mesin restart dan agar kita tidak perlu melakukan `sudo systemctl start mongod` berulang kali, kita dapat gunakan perintah `sudo systemctl enable mongod`.  