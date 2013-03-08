---
layout: post
title: "Dari WordPress ke Octopress"
date: 2013-02-10 03:15
comments: true
categories: 
- Chirps
tags:
- blog
---


#### *Returning to the dark age of world wide web...*

Kalau keliatan ada yang baru di blog saya ini, mungkin yang paling mencolok 
adalah desainnya berubah minimalis pake Skeleton. CSS template ini sebenarnya 
merupakan template "telanjang" yang seharusnya digunakan sebagai fondasi 
pengembangan desain kita sendiri, tapi saya biarkan apa adanya karena yang 
begini aja sudah cukup sedap dipandang mata.

<!-- more -->

Gak cuma itu, saya juga udah migrasiin platform blog ini [dari WordPress ke 
static HTML](http://jason.pureconcepts.net/2013/01/migrating-wordpress-octopress/). 
Anda gak salah baca, STATIC HTML, tanpa PHP, tanpa bahasa 
interpreter apapun, hanya HTML, CSS, dan JavaScript, tanpa database!

Kembali ke cara bikin web jaman purbakala? Nggak juga, karena sudah ada HTML 
generator khusus untuk keperluan ngeblog cara nyentrik ini, Jekyll namanya. 
Tapi berhubung pake Jekyll ini lumayan *njlimet*, saya pilih alternatif dengan 
Octopress yang merupakan *blogging framework* yang ngebungkus(wrapping) Jekyll.


#### Cara ngepost entri gimana?

Semua entri saya tulis dalam file *plain text* (awam: *file notepad*) yang akan 
di-*generate* (di komputer sendiri) oleh Octopress menjadi sekumpulan file HTML 
yang siap di-upload ke web hosting kita. 


#### Apa salahnya WordPress (self-hosted) sih? Kok ditinggalin?

I love WordPress, it's the most awesome blogging CMS. Tapi... *bloated*-nya 
itu loh yang gak nahan :| Kadang pake WordPress cuma buat ngeblog (fokus di 
konten) itu rasanya kayak berangkat ngampus pake helikopter, efektif
tapi berat. Selain itu...

0. WordPress ukurannya segede gaban! Extensible, tapi agak kurang kepake buatku.
0. Banyak pilihan plugin == Banyak celah buat malware. Siapa yang tau kalau 
   plugin yang kita install ternyata berisi malware ato celah yang ngebuka jalan
   hacker buat ngapa-ngapain blog kita?
0. Kadang buat hal trivial(sepele) aja butuh plugin
0. *Not so spam-proof*. Udah pake Akismet masih tetep kebanjiran spam, entah 
   celah dari mana :|
0. WordPress harus sering-sering update biar aman dari *security flaws*
0. Struktur databasenya ribet! Malesin lah kalo disuruh beresin isinya, apalagi
   kalo udah kebanjiran spam :|
0. Pasaran :p /*ditabok*


#### Keuntungan Octopress dibanding WordPress?

0. Loading blog super cepat, secepat web servermu dalam ngeload konten statis.
0. Karena ditulis dalam plain text(saya pake markdown), semua entri blog bisa 
   dengan mudah dilacak revisi/perubahannya pake Git/SVN.
0. Plain text itu bahasa universal, dan diakui sebagai bagian penting dari [Unix
   Philosophy](http://en.wikipedia.org/wiki/Unix_philosophy) B-)
0. Mau ngetik entri baru plus formattingnya gak perlu buka browser, dari notepad
   aja juga bisa.
0. Pindahan blog ke lain web hosting tinggal upload file.
0. Gak perlu import-export database MySQL buat pindahan blog.
0. Hemat space web hosting ampe berkali lipat. Sekarang saya cuma pake 4 MB 
   space dari sebelumnya ~30 MB pas masih pake WordPress.
0. Gak perlu security patch, *wong isine HTML tok*, mau nyari celah 
   *vulnerability* dari mana? Kecuali *web server*-nya emang bolong-bolong. 
0. Gak pasaran, dan berasa makin geeky karena bisa blogging dari command line 
   :))


#### Terus gak enaknya apa dong?

0. Generate HTML-nya lumayan lemot juga kalo entri blog dah buanyak banget.
0. Entri gak bisa dikomentarin pengunjung, kan HTML statis. Kecuali pake 
   *commenting system* pihak ketiga macam Disqus atau IntenseDebate.
0. Gak bisa posting dari mobile, jadi pengen ngembangin sendiri cara buat ini :p
0. Gak cocok buat pemula atau casual blogger.


Udah dulu deh, kapan-kapan tak apdet kalo inget :p
