---
title: "Redis: 01 Mengenal Redis"
categories: "Redis"
tags: "Redis"
---

Redis adalah kata singkatan dari Remote Dictionary Server yang termasuk dalam keluarga NoSQL database berjenis key-value database. Redis menyimpan data-datanya di dalam memori atau RAM yang dikenal dengan in-memory database, sehingga proses menyimpan dan menerima data dapat berlangsung sangat cepat. Database ini dibuat oleh seorang pria asal Sicily, Italia bernama Salvatore Sanﬁlippo.  

![Salvatore Sanﬁlippo - Founder Redis](/assets/images/redis/redis-01-founder.png)

Beberapa keunggulan redis dibanding in-memory database [lainnya](https://en.wikipedia.org/wiki/List_of_in-memory_databases) adalah seperti value dapat berupa string, list, atau set (bagi yang mempelajari bahasa python tentu sudah tidak asing lagi), dapat melakukan push dan pop elemen, bisa melakukan perpotongan pada set, dan masih banyak lagi.  

Perusahaan yang mengadopsi redis di awal adalah Github dan Instagram. Penggunaan redis yang dinilai paling penting ada pada Twitter yang digunakan untuk cache beberapa ratus tweets baru dari setiap pengguna yang aktif.  

----

**Key-value database**

Dari sekian banyak database NoSQL, redis mengadopsi konsep struktur penyimpanan data bernama key-value database, yang bisa dibilang adalah konsep paling mudah dipahami dalam penyimpanan data, karena hanya ada key sebagai nama dan value sebagai isinya.  

<p align="center">
  <img src="/assets/images/redis/redis-01-key-value-stores.png" alt="Struktur Penyimpanan Key Value" title="Struktur Penyimpanan Key Value" />
</p>

Key-value juga sering disebut dengan dictionary atau hash table. Value yang berasosiasi dengan key dapat berupa string maupun number (angka).  