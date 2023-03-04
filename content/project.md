---
title: "Project"
noComment: true
---

Beberapa _project_ yang saya kerjakan baik itu _side-project_ maupun _project_ serius.

## 1. Jadwal Shalat API

* **Nama**: Jadwal Shalat API
* **Deskripsi**: API _Endpoint_ untuk mendapatkan perkiraan jadwal shalat berdasarkan _latitude_ dan _longitude_.
* **Link**: <https://api.shalat.manoedinata.me>
* **Link Dokumentasi / Kode Sumber**: <https://github.com/manoedinata/api.shalat.manoedinata.me>

Ini adalah API _Endpoint_ untuk mendapatkan hasil kalkulasi perkiraan waktu shalat, berdasarkan input _latitude_ dan _longitude_. Projek ini menggunakan Flask sebagai _web framework_ dan _library_ [PrayTimes](http://praytimes.org) (Python) [yang sudah saya modifikasi sedikit](https://github.com/manoedinata/PrayTimes) untuk kalkulasi jadwal shalat.

Salah satu modifikasi penting yang saya lakukan yaitu penambahan metode kalkulasi **Sihat Kemenag RI, Indonesia**, namun metode ini masih belum saya temukan tulisan maupun artikel yang menyatakan secara eksplisit rumus yang digunakan. Untuk saat ini saya menggunakan beberapa keterangan dari [JadwalSholat.org](https://jadwalsholat.org).

## 2. Jadwal Shalat Web UI

* **Nama**: Jadwal Shalat Web UI
* **Deskripsi**: Implementasi web UI dari [Jadwal Shalat API](https://api.shalat.manoedinata.me).
* **Link**: <https://shalat.manoedinata.me>
* **Link Dokumentasi / Kode Sumber**: <https://github.com/manoedinata/shalat.manoedinata.me>

Ini adalah implementasi Web UI dari API Jadwal Shalat yang saya buat sebelumnya. Website ini menggunakan file HTML statis agar tetap simpel dan ringan. Website ini dapat mengambil jadwal shalat dengan tanggal yang spesifik maupun _range_ tanggal.

Ketika dibuka, website meminta izin untuk mengakses lokasi pengguna. Jika diizinkan, website akan mengambil data lokasi yaitu latitude dan longitude lalu melakukan _request_ ke _Endpoint_ API.
