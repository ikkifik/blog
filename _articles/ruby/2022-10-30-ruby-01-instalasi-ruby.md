---
title: "Ruby: 01 Instalasi Ruby"
categories: "Ruby"
tags: "Ruby"
# notes: 28/10/2022 berhasil terinstall 
---

Berhubung saya ganti _environment_(laptop, azeekk) dan saya ingin mulai menulis kembali setelah vakum sekitar setahun, jadi saya perlu untuk menginstall ulang segala macam keperluan untuk _developing_ blog ini (yang baru saya ingat juga ketika ingin upload tulisan, huhu).  

Karena blog ini berbasiskan jekyll yang merupakan SSG dari Ruby jadi kita mulai instalasi ruby terlebih dahulu, untuk OS saya menggunakan Ubuntu 22.04 (sumber: [gorails](https://gorails.com/setup/ubuntu/22.04))

----

## Pre-requisite

Memasang curl dan menambahkan repository yarn  

```bash
# curl
sudo apt install curl

# yarn
curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -

curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -

echo "deb https://dl.yarnpkg.com/debian/ stable main" | \ 
sudo tee /etc/apt/sources.list.d/yarn.list
```

Lakukan repository update  

```bash
# update package repository
sudo apt update
```

Install package yang dibutuhkan untuk memasang ruby  

```bash
# requirement packages
sudo apt install git-core zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev nodejs yarn
```

----

## Install Rbenv

Clone repository github dari rbenv, daftarkan lokasi clone rbenv pada environment variables  

```bash
# installing rbenv (ruby version manager)
cd
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc # if you use zsh, change .bashrc > .zshrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc # if you use zsh, change .bashrc > .zshrc
exec $SHELL
```

Clone rbenv ruby-build, daftarkan juga lokasi ruby-build pada environment variables  

```bash
# Installing ruby using rbenv ruby-build
git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc # if you use zsh, change .bashrc > .zshrc
exec $SHELL
```

----

### Install Ruby (dengan rbenv)


Install ruby versi 3.1.2 dengan rbenv, lalu set default versi ruby untuk versi global OS  

 ```bash
 # Install ruby (latest version)
 rbenv install 3.1.2

 # set default ruby version
 rbenv global 3.1.2
 ```

----

### Cek hasil instalasi

```bash
# check ruby version
ruby -v
```

----

### Memasang bundler, gem package manager

```bash
# install bundler (gem)
gem install bundler 
```

