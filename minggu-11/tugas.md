Aplikasi Containerisasi dan Orkestra Layanan Mikro
==================================================

Tahap Pengaturan 
================

Melakukan Proses Mengkloning Repository :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_1.PNG)

Langkah 0: Tautan Dasar Skrip Extractor 
=======================================

Periksa cabang pada step0 dan daftarkan file di dalamnya :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_2.PNG)

Melihat isi dari File linkextractor.py dengan menjalankan perintah dibawah ini :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_3.PNG)

Skrip yang tampaknya sederhana ini mungkin bukan yang paling mudah dijalankan pada mesin yang tidak memenuhi persyaratannya. Jalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_4.PNG)

Ketika mencoba menjalankannya sebagai skrip, mendapatkan Permission denied error, akan dilakukan periksa pada error dengan menjalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_5.PNG)

Izin saat ini -rw-r - r-- menunjukkan bahwa skrip tidak dapat dieksekusi. Kita dapat mengubahnya dengan menjalankan chmod a + x linkextractor.py sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_6.PNG)

Langkah 1: Script Extractor Tautan Kontainer
============================================

Periksa cabang step1 dan daftarkan file di dalamnya dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_7.PNG)

Menambahkan satu file baru (i.e, Dockerfile) dan akan melihat isinya dengan menjalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_8.PNG)

Jalankan Perintah docker image build -t linkextractor:step1 :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_9a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_9b.PNG)

Jika build berhasil, kita harus dapat melihatnya di daftar gambar jalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_10.PNG)

Sekarang, mari kita jalankan container dengan gambar ini dan ekstrak tautan dari beberapa halaman web langsung sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_11.PNG)

Mencoba di halaman web dengan lebih banyak tautan di dalamnya sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_12a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_12b.PNG)

Langkah 2: Tautkan Modul Extractor dengan URI Lengkap dan Anchor Text
=====================================================================

Periksa cabang step2 dan daftarkan file di dalamnya sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_13.PNG)

Melihat script yang diperbaharui dengan menajalnkan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_14a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_14b.PNG)

Membuat gambar baru dan lihat perubahan ini, dengan menjalankan perintah :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_15a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_15b.PNG)

Menjalankan perintah docker image ls sebbagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_16.PNG)

Menjalankan container menggunakan tautanextractor: gambar step2, akan menghasilkan keluaran yang ditingkatkan dengan menjalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_17a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_17b.PNG)

Menjalankan sebuah container menggunakan tautan gambarextractor sebelumnya: step1 masih akan menghasilkan output yang lama sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_18a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_18b.PNG)

Langkah 3: Layanan Link Extractor API
=====================================

Periksa cabang step3 dan daftarkan file di dalamnya sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_19.PNG)

Melihat Dockerfile untuk melihat perubahan dengan menajalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_20.PNG)

Melihat file main.py yang baru ditambahkan:

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_21a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_21b.PNG)

Membangun image baru dengan perubahan di tempat sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_22a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_22b.PNG)

Kemudian jalankan container dalam mode terlepas (-d flag) sehingga terminal tersedia untuk perintah lain saat container masih berjalan. 
Perhatikan bahwa memetakan port 5000 dari container dengan 5000 host (menggunakan argumen -p 5000: 5000) agar dapat diakses dari host.
dan juga memberikan nama (--name = linkextractor) ke container untuk membuatnya lebih mudah melihat log atau menghapus container. Dengan Menjalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_23.PNG)

Menjalankan printah docker container ls sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_24.PNG)

Membuat permintaan HTTP dalam bentuk / api / <url> untuk server dan mengambil respons yang berisi tautan yang diekstrak sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_25.PNG)

Melihat log menggunakan ekstraksi nama tautan yang di tetapkan untuk container dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_26.PNG)

Melihat pesan yang dicatat ketika server muncul, dan entri dari log permintaan ketika menjalankan perintah curl. Sekarang  melakukan hapus container dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_27.PNG)

Langkah 4: Tautan Extractor API dan Layanan Front Web End
=========================================================

Periksa cabang step4 dan daftarkan file di dalamnya dengan menggunakan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_28.PNG)

Melihat file docker-compose.yml yang kita miliki sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_29.PNG)

Melihat file www / index.php yang menghadap pengguna dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_30.PNG)

Menjalankan perintah docker-compose up -d --build untuk menaikan layanan dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_31a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_31b.PNG)

Memeriksa daftar kontainer yang berjalan mengonfirmasi bahwa kedua layanan tersebut memang berjalan dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_32.PNG)

Akses Layanan API sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_33.PNG)

Modifikasi file www / index.php untuk mengganti semua kemunculan Link Extractor dengan Super Link Extractor sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_34.PNG)

Membersihkan Git tracking dengan menjalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_35.PNG)

Sebelum kita melanjutkan ke langkah selanjutnya kita harus mematikan layanan ini, dengan menjalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_36.PNG)

Langkah 5: Layanan Redis untuk Caching
======================================

Periksa cabang step5 dan daftarkan file di dalamnya sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_37.PNG)

Memeriksa Dockerfile yang baru ditambahkan di bawah folder ./www dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_38.PNG)

Selanjutnya, kita akan melihat file api / main.py server API tempat menggunakan cache Redis sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_39a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_39b.PNG)

Melihat file docker-compose.yml yang diperbarui dengan menjalanakn perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_40.PNG)

Menjalanakan perintah docker-compose up -d --build sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_41a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_41b.PNG)

Untuk memeriksa apakah layanan Redis digunakan atau tidak, kita dapat 
menggunakan eksekutif pembuatan docker yang diikuti oleh nama layanan redis dan perintah monitor Redis CLI seperti berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_42.PNG)

Sekarang kita tidak memasang folder / www di dalam container, perubahan lokal seharusnya tidak tercermin dalam layanan yang berjalan sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_43.PNG)

Verifikasi bahwa perubahan yang dibuat secara lokal tidak mencerminkan dalam layanan yang berjalan 
dengan memuat ulang antarmuka web dan kemudian mengembalikan perubahan seperti berikut ini :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_44.PNG)

Sebelum melanjutkan ke langkah berikutnya, matikan layanan dengan menggunakan perintah berikut ini :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_45.PNG)

Langkah 6: Tukar Layanan API Python dengan Ruby
===============================================

Periksa cabang step6 dan daftarkan file di dalamnya sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_46.PNG)

Jalankan perintah cat api/linkextractor.rb sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_47.PNG)

File Ruby ini hampir sama dengan yang miliki di Python sebelumnya, kecuali, selain itu ia juga mencatat permintaan ekstraksi tautan dan kejadian cache yang sesuai. 
Dalam aplikasi arsitektur microservice, menukar komponen dengan komponen yang setara itu mudah asalkan harapan konsumen terhadap komponen tersebut tetap terjaga.

Melihat filedocker dengan menjalankan perintah cat api/Dockerfile :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_48.PNG)

Jalankan perintah cat docker-compose.yml sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_49a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_49b.PNG)

Jalankan perintah docker-compose up -d --build sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_50a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_50b.PNG)

Kita sekarang dapat mengakses API (menggunakan nomor port yang diperbarui) sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_51.PNG)

Sekarang, buka antarmuka web dengan mengeklik Link Extractor dan mengekstrak tautan dari beberapa URL. 
Coba juga untuk mengulangi upaya ini untuk beberapa URL. Jika semuanya baik-baik saja, aplikasi web harus bersikap seperti sebelumnya tanpa memperhatikan perubahan apa pun dalam layanan API (yang sepenuhnya diganti).

Kita dapat mematikan layanan sekarang dengan perintah sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_52.PNG)

Agar layanan tidak hilang dan bertahan di log jalankan perintah berikut cat logs/extraction. :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_53.PNG)

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-11/Capture_53a.PNG)

Kesimpulan 
==========

Praktik diatas dimulai dengan skrip Python sederhana yang mengikis tautan dari URL laman web yang ada.
mdengan enunjukkan berbagai kesulitan dalam menjalankan skrip. kemudian mengilustrasikan betapa mudahnya menjalankan dan 
membuat skrip menjadi mudah dikemas. Pada langkah selanjutnya secara bertahap mengembangkan skrip menjadi tumpukan aplikasi 
multi-layanan. Dalam proses tersebut kami mengeksplorasi berbagai konsep arsitektur layanan mikro dan bagaimana alat Docker 
dapat membantu dalam menyusun tumpukan multi-layanan. Akhirnya, kami mendemonstrasikan kemudahan pertukaran komponen layanan mikro dan 
kegigihan data.


