---
comments: true
date: 2011-04-05 16:42:50
layout: post
slug: menginstall-office-2007-di-lucid-dengan-playonlinux
title: Menginstall Office 2007 di Lucid dengan PlayOnLinux
wordpress_id: 487
categories:
- Computer and Internet
tags:
- linux
- software
- ubuntu
---

Salah satu aplikasi non-linux-available yang sangat saya butuhkan untuk keperluan sehari-hari adalah Microsoft Office, terutama Word. Okelah di Linux ada OpenOffice, LibreOffice, AbiWord, dan sebagainya, tapi gimana dengan konsistensi tampilan? Tidak jarang format docx milik saya jadi berantakan ketika dibuka di OpenOffice, dan sering kali saya bekerja tidak sendiri. Misalnya aja ngerjain laporan yang kerjanya keroyokan atau perlu dioper ke rekan lain untuk direvisi. Karena saya rada perfeksionis, konsistensi penyajian data adalah sangat penting. Ngomong-ngomong soal konsistensi, kayaknya saya perlu belajar bikin paper pake LaTeX :D

<!-- more -->

Karena pemakaian komputer saya sehari-hari berpusat di OS Linux dengan distro Ubuntu Lucid Lynx, berpindah ke OS tetangga hanya untuk sedikit merivisi laporan atau mengedit file .psd adalah sesuatu yang sangat merepotkan, terlebih dengan maha-lemot-nya Windows Vista saya yang kebetulan original itu.


> PlayOnLinux is a piece of sofware which allows you **to easily install and use** numerous **games and apps designed to run with Microsoft® Windows®.**




> PlayOnLinux is a front-end for wine. It permits you to install Windows Games and softwares on Linux.


![PlayOnLinux](http://www.playonlinux.com/images/logos/logo48.png)

Saya sudah mencoba menginstall Office 2007 menggunakan wine tapi selalu gagal di proses instalasi. Ternyata dengan PlayOnLinux masalah tersebut dapat diatasi. Mungkin ada ketidakcocokan dengan versi wine yang saya pakai, dan menurut pengamatan saya, PlayOnLinux mengatasi masalah tersebut dengan berperan sebagai _front-end version & prefix manager_ bagi wine. Jadi ketika saya mencoba menginstall Office 2007, PlayOnLinux akan otomatis memilihkan versi wine yang sesuai beserta library-library yang dibutuhkan.



Berikut langkah-langkahnya:


## 1. Install PlayOnLinux


Saya sangat merekomendasikan anda untuk menginstall PlayOnLinux versi terbaru.

[code lang="bash"]
wget -q "http://deb.playonlinux.com/public.gpg" -O - | sudo apt-key add -
sudo wget http://deb.playonlinux.com/playonlinux_maverick.list -O /etc/apt/sources.list.d/playonlinux.list
sudo apt-get update
sudo apt-get install playonlinux

[/code]


## 2. Install Office 2007


Buka PlayOnLinux dan klik 'Install'. Klik 'Refresh' bila diperlukan (list software belum diload)

[caption id="attachment_492" align="aligncenter" width="300"][![Pilih Microsoft Office 2007](http://octopress.dev/uploads/playonlinux-1-300x233.png)](http://octopress.dev/uploads/playonlinux-1.png) Pilih Microsoft Office 2007[/caption]

Cari Microsoft Office 2007 di menu Office dan klik Apply. Bisa dilihat kalau Access, Groove, dan Outlook tidak bisa jalan di atas Wine. Ketika anda mengklik Apply mungkin PlayOnLinux akan mendownload dulu versi Wine yang bisa digunakan untuk menjalankan Office 2007 dan membuatkan sebuah _wine prefix_ baru untuk itu.

Masukkan path tempat installer Office 2007 berada ketika diminta, dan lanjutkan terus hingga Installer Office 2007 dijalankan. Jangan lupa untuk tidak menginstall Microsoft Access, Groove, dan Outlook karena akan sia-sia :D


![](http://octopress.dev/uploads/ms-2007-300x156.png)


Di akhir instalasi mungkin PlayOnLinux akan mendownload lagi beberapa library yang dibutuhkan. Akhirnya paket Office 2007 anda siap dijalankan dari gnome menu atau shortcut di desktop. Sedikit tips, anda perlu menambahkan permission +x pada icon di desktop yang dibuat PlayOnLinux agar bisa dijalankan.





[caption id="attachment_503" align="aligncenter" width="286"][![Microsoft Word on My Lucid Laptop](http://octopress.dev/uploads/word-on-lucid-286x300.jpg)](http://octopress.dev/uploads/word-on-lucid.jpg) Microsoft Word on My Lucid Laptop[/caption]


> catatan: cara ini tidak hanya untuk Office, namun juga untuk aplikasi-aplikasi lain yang disupport oleh PlayOnLinux :)
