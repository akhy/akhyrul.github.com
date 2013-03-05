---
comments: true
date: 2010-03-28 19:11:24
layout: post
slug: mencoba-berbagai-code-editor-di-penguin
title: Mencoba Berbagai Code Editor di Penguin
wordpress_id: 145
categories:
- Computer and Internet
tags:
- linux
- programming
- review
- software
---

[![i need a nice yet powerful code editor](http://octopress.dev/uploads/webcode.jpg)](http://octopress.dev/uploads/webcode.jpg)Ide untuk menulis posting ini bermula ketika saya tengah mengerjakan theme wordpress yang mungkin sedang anda lihat sekarang. Bila di header blog ini ada sesosok cewek berseragam sekolah jepang yang menenteng sebuah katana sembari berlari, nah itulah hasil pertama kali saya melakukan coding secara serius di platform linux (tepatnya Ubuntu Karmic). _Baidewei_ kalo mau tau, nama theme-nya _Monochrome Kiss_ yang terinspirasi dari lagu _Monokuro no Kisu_ oleh _Sid_ yang kebetulan diputer pas baru kelar finishing jQuery-nya.

<!-- more -->



* * *

[spoiler]

Oke, cukup curcolnya :P Salah satu hal yang cukup memberatkan saya untuk coding di Linux adalah tidak adanya dukungan native [Notepad++](http://notepad-plus.sourceforge.net/) terhadap platform selain Windows meskipun sifatnya opensource. Padahal program cilik, lightweight, nan powerful tersebut telah menemani saya _coding segala bahasa_ selama terpuruk di _sistem operasi berpartisi NTFS_ gegara terjadi overlapping partisi yang menyebabkan HD saya tak terbaca oleh oknum OS turunan Unix itu :( Namun, akhirnya pemartisian ulang sukses dilakukan tanpa was-was setelah memindahkan puluhan GB data koleksi ke HD eksternal yang dirampas dengan suka cita dari [Arkham](http://plurk.com/eightis). Then... here i am, Linux i'm coming~! _*teriak lebay*_

Ehm, curcol lagi _*lirik paragrap sebelumnya*_ ya? Ketiadaan Notepad++ tidak menyurutkan semangat saya untuk tetap berusaha menjadikan Penguin sebagai OS untuk pemakaian sehari-hari. [Wine](http://www.winehq.org/)? No way! I don't drink! *eh?* Sebisa mungkin saya inginnya sih pake program yang native untuk Penguin (padahal karena tampilan jendela di Wine yang jelek). Gedit, text editor kebangsaan desktop [Jembalang](http://www.winehq.org/) meskipun bisa dikustomisasi dan cukup powerful, saya membiarkannya apa adanya agar tetap ringan sebagai text editor default. Yang saya butuhkan sekarang adalah _CODE EDITOR_. Hasil bertapa dengan koneksi kampus yang agak mending dibanding telkomflash, membuahkan informasi beberapa code editor yang top recommended.

[/spoiler]

Fyi, untuk code editor ini preferensi saya adalah yang semirip mungkin dengan notepad ples ples. Setidaknya ada syntax highlighting, code folding, indentation guide, plus file browser terintegrasi.  Automatic code/tag completion menurut saya terlalu merepotkan bagi yang lebih suka ngetik manual semua kodenya. Yah, semuanya tergantung selera. Berikut sedikit reviewnya :)



* * *




### gEdit


(`apt-get install gedit`)

Terinstall secara default pada Ubuntu dan semua distro dengan desktop Gnome. Ini tipe aplikasi favorit saya, simpel secara default namun bisa dikustomisasi menjadi super powerful. Yang menjadi nilai plus adalah dukungan plugin dan sifat customizable-nya yang cukup luas.  Meskipun begitu, saya membiarkannya tetap simple dan ringan untuk pemakaian sebagai teks editor, ya buat catatan-catatan kecil begitu lah.


> Lebih lanjut bisa anda baca artikel berikut: [Customizing gedit as a Web Developer's IDE](http://www.micahcarrick.com/09-29-2007/gedit-html-editor.html) dan [Textmate-like Gedit in few steps](http://grigio.org/textmate_gedit_few_steps)




### **Blue Fish** web development studio


(`apt-get install bluefish`)

Code editor yang pertama kali terlintas di benak saya ketika mencari alternatif gedit. Sesuai namanya, editor ini memfokuskan diri untuk pengembangan web. Tak heran bila shortcut-shortcut tag html, WYSiWYG editor, dan file browser sudah terintegrasi di dalamnya. Meskipun begitu, Blue Fish juga mendukung syntax highlihting berbagai source code lain kok. Sayangnya untuk indentasi saya agak kebingungan dengan BlueFish ini, tidak ada guide untuk setiap penekanan tombol tab. _Code folding_ juga tidak ada (atau saya yang gak nemuin?)


> Fitur Bluefish bisa ditemukan di situs resminya: [http://bluefish.openoffice.nl/features.html](http://bluefish.openoffice.nl/features.html)




### **jEdit** programmer's text editor


(`apt-get install jedit`)

Tidak seperti Blue Fish yang spesialis web, jEdit dari namanya sih keliatan lebih universal. Anda butuh java untuk menjalankannya, dan itu berarti multiplatform (hey, did you spot _'j'_ in the name?). Yang pertama terpikir oleh saya begitu menjalankannya adalah tampilannya yang _awful_. Namun bisa diakali dengan mengganti opsi interface agar menggunakan library GTK alih-alih Java Swing. Satu lagi, font pada bagian editor tampak tidak mulus dan pecah-pecah. Awalnya saya pikir masalah ada di font, namun setelah utak-atik lebih lanjut ditemukan bahwa setting default untuk anti-aliasing-nya adalah off. Silakan anda cari sendiri dibagian opsi.


Beberapa fitur jEdit yang dikutip [dari sini](http://www.jedit.org/index.php?page=features).


> 
	
>   * Plugins can turn jEdit into a very advanced XML/HTML editor, or a full-fledged IDE, with compiler, code completion, context-sensitive help, debugging, visual diff, and many language-specific tools tightly integrated with the editor.
> 
	
>   * Combines the best functionality of Unix, Windows and MacOS text editors.
> 
	
>   * Runs on any operating system with a Java 2 version 1.3 or higher virtual machine - this includes MacOS X, OS/2, Unix, VMS and Windows
> 






### **SciTe** Scintilla based Text Editor


(`apt-get install scite`)

Saya belum mencoba lebih jauh text editor ini karena cuma kebetulan nemu rekomendasi di forum. Cukup ringan, bersih, dan bisa jalan di Penguin maupun Jendela. Selain itu SciTE menggunakan library scilexer yang juga digunakan oleh Notepad++, meskipun saya belum begitu mengerti kegunaannya :P

Selebihnya? Silakan coba sendiri atau kunjungi situs resminya di [http://www.scintilla.org/](http://www.scintilla.org/)


### Editra


([http://editra.org/](http://editra.org/))

Masih dalam pengembangan, wajar bila belum tersedia dalam repository resmi. Lagi-lagi rekomendasi untuk program ini saya dapat di forum oleh orang yang akhirnya mengaku bahwa dialah developernya. Bisa jalan di berbagai platform (Windows, Mac, Unix) dan dibangun menggunakan Python dan wxWindows. Belum saya coba lebih jauh :)


> Untuk menginstall ketikkan perintah di direktori installer: `python setup.py install`




### **Geany**


(`sudo apt-get install geany`)

Bukan sekedar code editor. Aplikasi dengan logo lampu ajaib aladin ini sebenarnya adalah sebuah Integrated Development Environment (IDE) yang sangat ringan dan gampang dikustomisasi. Entah kenapa feel saya paling pewe kalo pake Geany. Karena cukup memuaskan saya, akhirnya Geany lah yang saya pilih untuk menemani coding web sehari-hari, kecuali untuk Java yang saya serahkan pada NetBeans IDE (efek praktikum OOP & AI).


> Berbagai extras untuk kustomisasi Geany bisa diperoleh di sini: [http://www.geany.org/Download/Extras](http://www.geany.org/Download/Extras)




* * *

.
.


> Sesungguhnya semua kembali pada selera masing-masing. Silakan anda tentukan pilihan yang sesuai kenyamanan anda. Saya hanya berbagi pengalaman ketika "hunting" code editor di Pinguin. Ada pendapat lain?

(worship)


.
