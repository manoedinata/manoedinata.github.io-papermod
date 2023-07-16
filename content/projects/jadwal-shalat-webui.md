---
title: "Jadwal Shalat Web UI"
noComment: true
---

> Web UI Jadwal Shalat, menggunakan Jadwal Shalat API.

<!--more-->

Ini adalah implementasi Web UI dari API Jadwal Shalat yang saya buat sebelumnya. Website ini menggunakan file HTML statis agar tetap simpel dan ringan. Website ini dapat mengambil jadwal shalat dengan tanggal yang spesifik maupun _range_ tanggal.

Ketika dibuka, website meminta izin untuk mengakses lokasi pengguna. Jika diizinkan, website akan mengambil data lokasi yaitu latitude dan longitude lalu melakukan _request_ ke _Endpoint_ API.
