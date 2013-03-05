---
comments: true
date: 2010-10-24 21:09:42
layout: post
slug: mencegah-jquery-konflik-dengan-library-lain
title: Mencegah jQuery konflik dengan library lain
wordpress_id: 400
categories:
- Web Development
tags:
- jquery
- tips
---

[![Numpang Promosi](http://octopress.dev/uploads/jquery-workshop-300x211.jpg)](http://octopress.dev/uploads/jquery-workshop.jpg)




Kadang kita butuh lebih dari satu _Javascript Library_ dalam satu waktu. Dalam kasus saya beberapa hari yang lali, plugin yang saya butuhkan ternyata hanya bisa digunakan dengan library Mochikit. Kebetulan berbeda dengan library yang saya gunakan untuk website yang sama, yaitu jQuery.<!-- more -->


Ketika menggunakan beberapa library JavaScript bersamaan terkadang muncul konflik yang agak sulit untuk didebug. Entah saya yang bego, yang jelas saya menghabiskan sampe satu jam untuk ngoprek kode hanya untuk akhirnya tepok jidat menyadari kalau terjadi konflik antara Mochikit dan jQuery (doh)

Simpelnya pencegahan konflik semacam itu bisa diatasi dengan menambahkan Javascript di bagian head sebagai berikut:

[code lang="js"]
jQuery.noConflict();
[/code]

Untuk selanjutnya semua pemanggilan jQuery yang menggunakan tanda dolar ("$") kita ganti menjadi "jQuery". Misalnya begini:

[code lang="js"]
jQuery('terserah').hide();
[/code]

Alternatif lain, bila tetap ingin jQuery dapat dipanggil dengan nama singkat bisa dilihat contoh di bawah:

[code lang="js"]
var $j = jQuery.noConflict();
$j('terserah').hide();
[/code]

Gampang kan? ;)
