---
title: "GCP: Membuat Apps Credential Keys"
categories: "Cloud"
tags: "Cloud"
---

Google cloud credential keys berguna ketika kita hendak menjalankan aplikasi yang ada di google cloud dari luar lingkungan google cloud. Semacam memberikan identitas untuk aplikasi kita agar bisa mengakses sebuah aplikasi-aplikasi milik google cloud, contohnya seperti API.  

<!-- Tulisan ini sebagai pendukung bagi yang ingin menjalankan [tools ekstrak data landsat dari GCP Public Data](/project/2022/11/25/landsat-8-extraction-tools) yang ada di blog ini.   -->

Langkah demi langkahnya sebagai berikut.  

1. Buka akun google cloud console, [console.cloud.google.com](console.cloud.google.com)
   
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-01.png)

2. Pilih project google cloud (di pojok kiri atas sebelah logo "Google Cloud")
   
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-02.png)
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-03.png)
   
3. Pada sidebar di sebelah kiri, arahkan kursor pada menu _APIs & Services_ maka akan muncul sub-menu, pilih Credentials.
   
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-04.png)
   
4. Pada halaman ini klik tombol `+ CREATE CREDENTIALS` lalu pilih _Service account_.
   
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-05.png)
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-06.png)
   
5. Masuk pada halaman _Create Service Account_, di sini kita masukkan nama service account-nya, boleh juga dideskripsikan fungsi dari credential service accountnya pada kolom deskripsi.
   
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-07.png)
   
6. Jika sudah klik tombol `Done`. (untuk step yang lain opsional, dapat di tambahkan sesuai kebutuhan.)
   
7. Selanjutnya kita akan diarahkan kembali menuju halaman _APIs & Services_, klik tombol dengan ikon pensil pada project yang barusan kita buat.
   
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-08.png)
   
8. Kita akan diarahkan ke halaman _IAM & Admin_, pada bagian tab pilih _Keys_, kita akan lakukan export file `.json`
   
   ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-09.png)
   
9.  Klik tombol `ADD KEY` -> `Create new key`.
   
    ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-10.png)
   
10. Jendela baru akan terbuka, lalu pilih JSON dan klik `Create`.
   
    ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-11.png)
   
11. Selesai, browser akan otomatis mendownload credentials key yang dapat digunakan pada project kita yang memanfaatkan fitur google cloud.

    ![google-cloud-console-pages](/assets/images/gcp/create-credential-keys-12.png)

----

<!-- Jika mengikuti tulisan ini untuk dapat menjalankan [tools ekstrak data landsat dari GCP Public Data](/project/2022/11/25/landsat-8-extraction-tools), silakan pindah file `.json` tadi ke direktori yang sama dengan direktori tools tersebut.   -->

Sekian dan terimakasih, semoga bermanfaat, _ciao!_