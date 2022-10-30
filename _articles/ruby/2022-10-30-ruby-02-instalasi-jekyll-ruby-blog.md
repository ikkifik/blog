---
title: "Ruby: 02 Instalasi Jekyll - Ruby Static Site Generator(SSG)"
categories: "Ruby"
tags: "Ruby"
---

Setelah ruby berhasil terpasang, langkah selanjutnya yaitu memasang jekyll. Karena saya sedang malas berbasa-basi tapi ingin menulis, jadi kalimat pembukanya sampai di sini saja ya, hehe.  

Instalasi masih dilakukan di OS yang sama yaitu Ubuntu 22.04 (source: [jekyllrb](https://jekyllrb.com/docs/installation/)).

----

### Set default path gem

Perintah berikut akan menambahkan environment variable gem pada file .bashrc (.zshrc apabila terminal menggunakan zsh)  

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc # if you use zsh, change .bashrc > .zshrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc # if you use zsh, change .bashrc > .zshrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc # if you use zsh, change .bashrc > .zshrc
source ~/.bashrc
```

----
### Install jekyll dengan gem

```bash
# Install jekyll melalui gem
gem install jekyll

# (opsional) Install bundler gem manager, apabila belum terinstal
gem install bundler
```

----
**Catatan kaki:** apabila sudah mengikuti instalasi ruby pada tulisan sebelumnya, bundler sudah kita pasang, jadi tidak perlu memasang bundler kembali