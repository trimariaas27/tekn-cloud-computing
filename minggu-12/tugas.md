Docker Orchestration Hands-on Lab
=================================

Bagian 1: Apa itu Orkestrasi ?
==============================

Jadi, apa itu orkestrasi? Yah, orkestrasi mungkin paling baik digambarkan menggunakan contoh. Katakanlah Anda memiliki aplikasi yang memiliki lalu lintas tinggi bersama dengan persyaratan ketersediaan tinggi. Karena persyaratan ini, Anda biasanya ingin menggunakan setidaknya 3+ mesin, aplikasi Anda masih dapat diakses 
Menyebarkan aplikasi Anda tanpa Orkestrasi biasanya sangat memakan waktu dan rawan kesalahan, karena Anda harus secara manual SSH ke setiap mesin, mulai aplikasi Anda, dan kemudian terus mengawasi hal-hal untuk memastikan itu berjalan seperti yang Anda harapkan.

Salah satu fitur keren Orkestrasi dengan Docker Swarm, adalah dapat menggunakan aplikasi di banyak host dengan hanya satu perintah (setelah mode Swarm diaktifkan). Plus, jika salah satu node pendukung mati di Docker Swarm Anda.
Jika Anda biasanya hanya menggunakan docker run untuk menyebarkan aplikasi Anda, maka kemungkinan besar Anda akan mendapat manfaat dari menggunakan Docker Compose, Docker Swarm mode, atau keduanya Docker Compose dan Swarm.

Bagian 2: Konfigurasikan Swarm Mode
===================================

Contoh menjalankan berbagai hal secara manual dan pada satu host adalah membuat container baru pada node1 dengan menjalankan docker run -dt ubuntu sleep infinity :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar1a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar1b.png)

Memverifikasi container dengan menjalankan perintah docker ps pada node1 :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar2.png)

Langkah 2.1 - Create a Manager node
-----------------------------------

Jalankan docker swarm init pada node1.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar3a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar3b.png)

Menjalankan perintah docker info untuk memverifikasi bahwa node1 berhasil dikonfigurasi sebagai node swarm manager.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar4a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar4b.png)

Langkah 2.2 - Join Worker nodes to the Swarm
--------------------------------------------

Melakukan prosedur berikut pada node2 dan node3. Menjelang akhir prosedur, akan beralih kembali ke node1.
Salin perintah dari output pada node1. Pada node2 dan node3 akan terlihat seperti dibawah ini:

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar5.png)

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar6.png)

Setelah menjalankan ini pada node2 dan node3, beralih kembali ke node1, dan jalankan docker node ls untuk memverifikasi bahwa kedua node adalah bagian dari Swarm. 

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar7a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar7b.png)

Bagian 3: Menyebarkan aplikasi di beberapa host
===============================================

Sekarang setelah memiliki swarm up dan running, sekarang saatnya untuk menggunakan sleep aplication yang sangat sederhana.

Anda akan melakukan prosedur berikut dari node1.

Langkah 3.1 - Menyebarkan komponen aplikasi sebagai layanan Docker
------------------------------------------------------------------

Menjalankan perintah  sleep sebagai Layanan di Docker Swarm :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar8.png)

Verifikasi bahwa pembuatan layanan telah diterima oleh manajer Swarm dengan menajalankan perintah docker service ls :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar9.png)

Bagian 4: Skala aplikasi
========================

Dapat menjalankan prosedur berikut pada node1.
Skala jumlah kontainer dalam layanan sleep-app  7 dengan pembaruan layanan dengan menjalankan perintah docker service update –replicas 7 sleep-app :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar10a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar10b.png)

Menjalankan perintah docker service ps  sleep-app, dapat melihat container muncul secara real time :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar11a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar11b.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar11c.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar11d.png)

Perhatikan bahwa sekarang ada 7 kontainer yang terdaftar. Mungkin diperlukan beberapa detik untuk container baru dalam layanan untuk semua ditampilkan. Kolom NODE memberi tahu di mana node container sedang berjalan.

Skala layanan kembali menjadi hanya empat kontainer dengan pembaruan layanan replika 4 perintah sleep-app :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/Gambar12a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar12b.png)

Verifikasi bahwa jumlah kontainer telah dikurangi menjadi 4 menggunakan perintah docker service ps sleep-app :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar13a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar13b.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar13c.png)

Bagian 5: Drain a node and reschedule the containers
====================================================

Lihatlah status node dengan menjalankan docker node ls pada node1.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar14a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar14b.png)

Mari kita lihat container yang telah Anda jalankan di node2.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar15.png)

Sekarang kembali ke node1 (manajer Swarm) dan mengambil node2 dari layanan. Untuk melakukan itu, kita jalankan kembali perintah docker node ls.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar16a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar16b.png)

Periksa status node

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar17a.png) 
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar17b.png)

Beralih kembali ke node2 dan lihat apa yang sedang berjalan di sana dengan menjalankan perintah docker ps :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar18.png)

Pada node2 tidak memiliki kontainer yang berjalan.

Terakhir, periksa lagi layanan pada node1 untuk memastikan bahwa kontainer dijadwal ulang. Anda harus melihat keempat kontainer berjalan di dua node yang tersisa dengan menjalankan perintah docker service ps sleep-app :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar19a.png) 
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar19b.png)

Membersihkan
============

Jalankan perintah docker service rm sleep-app pada node1 untuk menghapus layanan yang disebut myservice.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar20.png)

Jalankan perintah docker ps pada node1 untuk mendapatkan daftar kontainer yang berjalan.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar21a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar21b.png)

Jalankan docker swarm leave --force on node1.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar22.png)

Kemudian, jalankan docker swarm leave --force on node2.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar23.png)

Kemudian, jalankan docker swarm leave --force on node3.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar24.png)

Bagikan ini di → https://twitter.com/docker

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-12/gambar25.png)

