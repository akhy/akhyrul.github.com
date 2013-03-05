---
comments: true
date: 2010-08-16 06:17:53
layout: post
slug: memindahkan-blogroll-ke-page-wordpress-tanpa-harus-mengetik-manual
title: Memindahkan Blogroll ke Page WordPress Tanpa Harus Mengetik Manual
wordpress_id: 272
categories:
- Computer and Internet
tags:
- blog
- tips
- wordpress
---

Berhubung lagi demen sama tampilan simpel, maka saya mau gak mau harus melakukan sweeping _sidebar_ :D Salah satu yang cukup banyak dan akan selalu bertambah banyak adalah widget blogroll. Mau gak ditampilin sayang, ditampilin juga boros tempat. Salah satu solusinya adalah dengan memindahkannya ke _page_ (ini salah satu jargon WordPress (WP), jangan diartikan sebagai halaman :) ). Kalo gak ngerti, kayak yang [di sini](http://akhyar.web.id/blogroll) lho ;)

<!-- more -->Setelah _googling_ sana-sini solusi yang saya temukan kebanyakan menyarankan untuk membuat _custom template_. Nah lo, terlalu teknis ya? _Ember_, soalnya harus ngedit-ngedit kode lagi. Bagi yang alergi coding atau kurang ngerti jeroannya WordPress, cara ini terlalu ribet. Kadang ada yang menempuh jalan manual dengan mengetikkannya manual di _page_ baru yang dikasih nama 'Blogroll' misalnya. Waduh, kalo blogrollnya udah banyak jadi ribet dong? Untuk pengguna WordPress _self-hosted_ (baca: install sendiri, bukan yang di WordPress.com) ada cara yang lebih simpel, dengan syarat ngerti caranya install _plugin_. Masa udah make WordPress _self-hosted_ gak bisa nginstall plugin sih? ;)

Seharusnya bagi pemakai WordPress yang udah berpengalaman pasti bisa menebak alur cerita posting ini :D

Yup, emang pake plugin. Yang saya pakai di sini adalah **WP Render Blogroll Links** ([http://wordpress.org/extend/plugins/wp-render-blogroll-links/](http://wordpress.org/extend/plugins/wp-render-blogroll-links/))

Gini cara nginstallnya lewat dashboard:



	
  1. Login ke dashboard WP, masuk ke menu P**lugins > Add New**

	
  2. Ketikkan `WP Render Blogroll Links` di kolom search, lalu klik Search Plugins.

	
  3. Setelah ketemu. Klik aja install now dan ikuti langkah selanjutnya. Standar lah, paling masukin akun FTP buat download dari server pluginnya. ;)

	
  4. Kalo sudah diinstall jangan lupa diaktifin di menu **Plugins > Plugins**.


Kalau sudah, bikin page baru atau edit page yang sudah ada kalau terlanjur bikin blogroll manual :-"

Untuk memunculkan list blogroll di page tersebut masukkin aja **`[ wp-blogroll ]`**`** **`(hilangin spasinya) di page itu. Informasi teknis lebih lanjut ada di link yang sudah saya kasih sebelumnya. Kalo udah dipublish nanti jadinya kayak [di page ini](http://akhyar.web.id/blogroll/).

Selamat mencoba! (gym)

**
**
