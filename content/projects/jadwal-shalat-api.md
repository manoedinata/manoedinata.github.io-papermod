---
title: "Jadwal Shalat API"
noComment: true
---

> API untuk mendapatkan hasil kalkulasi perkiraan waktu shalat, berdasarkan input _latitude_ dan _longitude_. 

<!--more-->

Project ini merupakan sebuah API _Endpoint_ sederhana untuk mendapatkan hasil kalkulasi perkiraan waktu shalat, berdasarkan input _latitude_ dan _longitude_. Projek ini menggunakan Flask sebagai _web framework_ dan _library_ [PrayTimes](http://praytimes.org) (Python) [yang sudah saya modifikasi sedikit](https://github.com/manoedinata/PrayTimes) untuk kalkulasi jadwal shalat.

Salah satu modifikasi penting yang saya lakukan yaitu penambahan metode kalkulasi **Sihat Kemenag RI, Indonesia**, namun metode ini masih belum saya temukan tulisan maupun artikel yang menyatakan secara eksplisit rumus yang digunakan. Untuk saat ini saya menggunakan beberapa keterangan dari [JadwalSholat.org](https://jadwalsholat.org).
