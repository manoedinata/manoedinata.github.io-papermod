---
title: "Pengalaman Memperbaiki CCTV Yang Tidak Mendeteksi HDD"
date: 2022-12-31
---

> Pengalaman panjang memperbaiki DVR CCTV... dan ternyata diluar ekspektasi!

<!--more-->

# Pembuka
Suatu sore yang tenang di rumah saya.

Saya sedang membaca sebuah novel fiksi di ruang tamu, hingga...

*Deg!*

Listrik tiba-tiba padam. Namun saya tidak kaget. Daerah rumah saya memang seringkali mengalami pemadaman. Oke, saya biarkan saja. *Toh*, nanti juga hidup sendiri.

Selang beberapa menit kemudian, listrik kembali hidup. Saya kira hanya itu, sampai...

*Tit tiit tiit tiit tiiit!*

Beberapa bunyi *beep* terdengar yang berasal dari DVR CCTV rumah. *Oh tidak...* Saya tahu bunyi itu. Bunyi yang menandakan kalau terdapat masalah pada DVR, entah itu pada penyimpanan atau jaringan.

![ab67616d0000b273950359444321d635b59838b3.jpg](https://i.postimg.cc/HnRpzLtD/ab67616d0000b273950359444321d635b59838b3.jpg)

# Diagnosa

Saya beranjak ke lokasi DVR, dan hal yang pertama saya sadari yaitu indikator LED penyimpanan tidak menyala, yang artinya terdapat masalah pada media penyimpanan (*hard disk*). Untuk jaringan tidak ada masalah, karena DVR dapat mengakses Internet menggunakan kabel LAN secara normal, yang artinya masalah hanya pada penyimpanan.

Saya lalu membuka panel admin DVR dan menuju ke *tab* **Storage**, dan mendapati bahwa HDD yang terpasang tidak terdeteksi oleh DVR. Dapat diketahui dari ukuran HDD yang ada menunjukkan 0MB.

# Solusi

## 1: Restart DVR

Hal pertama yang saya coba sebagai solusi adalah dengan merestart / reboot DVR. Tentu, restart menjadi solusi paling efektif di dunia teknologi. Terlebih lagi pada *router* Internet...

[![akurat-20200717015456-203-FB7.jpg](https://i.postimg.cc/66ncrP6g/akurat-20200717015456-203-FB7.jpg)](https://postimg.cc/Lh4jRN13)

Restart sudah selesai, namun HDD masih tidak terdeteksi. Dari sini saya langsung beranggapan bahwa *disk* nya sendiri yang rusak. Mungkin karena 'kaget' saat listrik kembali hidup, jadi HDD nya 'ngadat' alias tidak mau berputar.

## 2: Cek Kabel Konektor

Mungkin kabelnya ada yang putus atau lepas. Saya memutuskan untuk membongkar DVR (dengan bantuan ayah saya, tentunya) untuk mengecek bagian penghubung HDD. Ternyata semuanya aman. Tidak ada yang lepas.

## 3: Mengganti HDD

Kebetulan saya punya satu HDD tidak terpakai yang saya temukan di toko ayah saya (yang juga dipasangi CCTV). Tapi kondisi nya tidak diketahui, apakah masih berfungsi atau tidak. *Well, it's worth a try!*

Saya lepas kabel konektor pada DVR lalu menghubungkannya ke HDD tadi, namun tetap tidak terdeteksi.

Sampai disini bertambah kesimpulan baru: Kedua HDD kemungkinan tidak berfungsi

## 4: Pengecekan HDD

Saya mempunyai pikiran untuk membeli HDD baru, namun kakak saya menyarankan untuk melakukan pengecekan terhadap kedua HDD tersebut (bawaan DVR dan HDD tidak terpakai) terlebih dahulu. Oke deh.

Saya menuju ke toko komputer terdekat dan meminta untuk melakukan pengecekan, mengingat saya tidak mempunyai komputer untuk melakukan pengecekan maupun kabel konverter (SATA 3.5 to USB).

Pengecekan pun dilakukan, dan hasilnya? Kedua HDD masih berfungsi! *Disk* terdeteksi dan dapat diakses, hanya saja perlu diformat terlebih dahulu. Tapi itu tidak menjadi perkara, karena HDD dapat diformat melalui DVR saat inisialisasi *disk*.

## 5: Pengecekan Keseluruhan

Akhirnya, saya memutuskan untuk membawa DVR ke toko komputer tadi untuk dilakukan pengecekan secara keseluruhan. Pengecekan pun kembali dilakukan. HDD nya, kabel data dan powernya. Tidak ada masalah. Pemilik toko kemudian mengatakan bahwa kemungkinan yang bermasalah adalah *main board* dari DVR.

## 6: Mengganti *Adaptor*

Tepat sebelum menyerah, terlintas di benak saya bahwa *adaptor* arus lah yang menjadi masalah. Saya meminta pemilik toko untuk mengganti *adaptor*, dan ternyata...

**HDD dapat terdeteksi** dan berfungsi seperti sebelumnya!

# Kesimpulan dan Penutup

Setelah melalui proses bongkar-pasang yang panjang, ternyata masalahnya terletak pada *adaptor* yang tidak berfungsi dengan baik, menyebabkan HDD tidak kuat berputar.

Pengalaman baru: Cek *adaptor* terlebih dahulu saat CCTV bermasalah. Hehe!
