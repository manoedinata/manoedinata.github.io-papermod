---
title: "Instalasi code-server, VS Code Versi Web"
date: 2023-01-01
---

> Tutorial singkat instalasi code-sever beserta konfigurasi NGINX

<!--more-->

# Pembuka
Pada suatu ketika, sempat terpikir di benak saya untuk memasang *code editor* yang dapat saya akses secara *online*. Hal ini tentu akan membuat kegiatan *ngoding* saya lebih fleksibel, karena saya tetap dapat ngoding dari mana saja dan kapan saja. Dan juga, pekerjaan saya akan tersimpan di *cloud server*, jadi *project* tetap dapat saya akses meskipun saya tidak sedang membawa *laptop*.

Karena *code editor* utama saya adalah **Visual Studio Code** (VS Code), maka saya memilih **code-server**, sebuah modifikasi dari VS Code yang memungkinkannya untuk dapat diakses melalui *browser*. Singkatnya, *code-server* dipasang pada suatu perangkat (seperti *cloud server*, *VM*, dan lain sebagainya) kemudian diakses melalui *browser*. Keren, *to*?

# Persiapan

Untuk dapat memasang *code-server*, kita memerlukan sebuah *server* atau perangkat **Linux** (OS lain mungkin dapat digunakan, namun Linux lebih utama) dengan **IP publik**. Kita memerlukan IP publik agar *code-server* dapat diakses dari luar *server*.

Disini saya menggunakan VM dari [IDCloudHost](https://idcloudhost.com), menggunakan OS Ubuntu 22.04.

Oh iya, pengguna baru akan mendapatkan saldo gratis sebesar **25.000**! Daftar disini: <https://console.idcloudhost.com/referral/0sckxq>

# Instalasi code-server

Untuk memasang code-server, kita dapat menggunakan [*script* instalasi otomatis resminya](https://coder.com/docs/code-server/latest/install#installsh).

```bash
curl -fsSL https://code-server.dev/install.sh | sh
```

Proses instalasi akan berjalan secara otomatis. Ditinggal *ngopi* saja, hehe.

Untuk semua metode pemasangan code-server, silahkan merujuk ke [dokumentasi instalasi](https://coder.com/docs/code-server/latest/install).

# Konfigurasi NGINX

code-server telah terpasang dan dapat diakses melalui IP publik *server*. Agar lebih keren, kita dapat mengatur penggunaan *domain* seperti **code.manoe.my.id** menggunakan reverse-proxy seperti [NGINX](https://nginx.org).

Contoh konfigurasi NGINX juga sudah disediakan di [dokumentasi resminya](https://coder.com/docs/code-server/latest/guide#using-lets-encrypt-with-nginx). Baik banget, deh!

Buat file di `/etc/nginx/sites-available/code-server`:

```bash
sudo nano /etc/nginx/sites-available/code-server
```

Lalu *paste*-kan konfigurasi berikut:

```nginx
server {
    listen 80;
    listen [::]:80;
    server_name code.manoe.my.id;

    location / {
      proxy_pass http://localhost:8080/;
      proxy_set_header Host $host;
      proxy_set_header Upgrade $http_upgrade;
      proxy_set_header Connection upgrade;
      proxy_set_header Accept-Encoding gzip;
    }
}
```

> Ganti code.manoe.my.id dengan domain yang diinginkan

Kemudian, aktifkan konfigurasi berikut dengan:

```bash
sudo ln -sf /etc/nginx/sites-available/code-server /etc/nginx/sites-enabled/code-server
```

Terakhir, restart NGINX:

```bash
sudo systemctl restart nginx
```

Selesai! code-server dapat diakses menggunakan domain.

# Penutup

Begitulah sedikit *tutorial* instalasi code-server. Konfigurasi dapat ditambah sesuai kebutuhan dan keinginan, seperti menggunakan SSL, menggunakan *proxy domain*, dan lain-lain.

Dengan adanya code-server tentu membuat kegiatan *ngoding* menjadi lebih fleksibel, karena dapat dilakukan dimana saja dan kapan saja.
