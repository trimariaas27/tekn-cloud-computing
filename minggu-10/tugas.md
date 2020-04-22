Docker Networking Hands-on Lab
==============================

Tugas:
======

Bagian 1 - Dasar-Dasar Jaringan
-------------------------------

Langkah 1: Perintah Jaringan Docker

Perintah docker network adalah perintah utama untuk mengonfigurasi dan mengelola jaringan kontainer. 
Jalankan perintah docker network dari terminal pertama :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar1.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar2.png)

Output yang dihasilkan dari menjalankan perintah menunjukkan bagaimana menggunakan perintah dan juga 
semua sub-perintah jaringan docker network. Seperti yang lihat dari output, docker network memungkinkan 
kita untuk membuat jaringan baru, mendaftar jaringan yang ada, memeriksa jaringan, dan menghapus jaringan. 
Perintah tersebut juga memungkinkan  untuk menghubungkan dan memutuskan docker dari jaringan.

Langkah 2: Daftar jaringan

Jalankan perintah docker network ls perintah untuk melihat jaringan kontainer yang ada pada host Docker saat ini.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar3.png)

Output di atas menunjukkan jaringan kontainer yang dibuat sebagai bagian dari instalasi standar Docker.
Jaringan baru yang di buat juga akan muncul di output dari hasil menjalakan perintah docker network ls.
Kita juga dapat melihat bahwa setiap jaringan mendapatkan ID dan NAME yang unik. Setiap jaringan juga dikaitkan dengan satu driver. 
Perhatikan bahwa jaringan "bridge" dan jaringan "host" memiliki nama yang sama dengan driver masing-masing.

Langkah 3: Periksa jaringan

Perintah docker network inspect bridge digunakan untuk melihat detail konfigurasi jaringan. 
Rincian ini meliputi; nama, ID, driver, driver IPAM, info subnet. Gunakan jaringan docker periksa <network> 
untuk melihat detail konfigurasi dari jaringan kontainer pada host Docker Anda. 

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar4.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar5.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar6.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar7.png)

Langkah 4: Daftar plugin driver jaringan

Perintah docker info menunjukkan banyak informasi menarik tentang pemasangan Docker.
Jalankan perintah docker info dan temukan daftar plugin jaringan.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar8.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar8a.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar9.png)

Bagian 2 - Jembatan Jaringan
----------------------------

Langkah 1: Dasar-Dasarnya

Setiap instalasi Docker yang bersih dilengkapi dengan jaringan yang disebut jembatan. 
Verifikasi ini dengan menjalkan perintah docker network ls.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar10.png)

Output di atas menunjukkan bahwa jaringan bridge dikaitkan dengan driver bridge. Penting untuk dicatat bahwa jaringan dan driver terhubung, tetapi mereka tidak sama. 
Output di atas juga menunjukkan bahwa jaringan bridge dicakup secara lokal. Berarti bahwa jaringan hanya ada pada host Docker ini. Ini berlaku untuk semua jaringan yang menggunakan driver bridge - driver bridge menyediakan jaringan host tunggal.
Semua jaringan yang dibuat dengan driver bridge didasarkan pada Linux bridge (a.k.a. switch virtual).

Instal dengan menjalankan perintah apk update dan gunakan untuk mendaftar bridge Linux di host Docker Anda. Anda dapat melakukan ini dengan menjalankan apk add bridge.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar11.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar12.png)

Lalu, daftarkan jembatan pada host Docker Anda, dengan menjalankan brctl show.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar13.png)

Output di atas menunjukkan bridge Linux tunggal yang disebut docker0. Ini adalah jembatan yang secara otomatis dibuat untuk jaringan. 
Anda dapat melihat bahwa saat ini tidak ada antarmuka yang terhubung.

Anda juga dapat menggunakan perintah ip a untuk melihat detail jembatan docker0.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar14.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar15.png)

Langkah 2: Hubungkan docker

Jaringan bridge adalah jaringan default untuk docker baru. Buat docker baru dengan menjalankan docker run -dt ubuntu sleep infinity.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar16.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar17.png)

Perintah ini akan membuat docker baru berdasarkan Ubuntu. Kita dapat memverifikasi contoh docker dengan menjalankan perintah docker ps :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar18.png)

Karena tidak ada jaringan yang ditentukan pada perintah docker run, kontainer akan ditambahkan ke jaringan bridge.

Jalankan perintah brctl show lagi.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar19.png)

Perhatikan bagaimana bridge docker0 sekarang memiliki antarmuka yang terhubung. Antarmuka ini menghubungkan bridge docker0 ke docker baru yang baru saja dibuat.

Kita dapat memeriksa jaringan bridge lagi, dengan menjalankan perintah docker network inspect bridge :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar20.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar21.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar22.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar23.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar24.png)

Langkah 3: Uji konektivitas jaringan

Balasan di atas menunjukkan bahwa host Docker dapat melakukan ping kontainer melalui jaringan bridge. 
Masuk ke dalam docker, instal program ping, lalu ping www.github.com.
Pertama, kita perlu mendapatkan ID docker dimulai pada langkah sebelumnya. 
Anda dapat menjalankan perintah docker ps untuk mendapatkan itu :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar25.png)

Mari ping www.github.com dengan menjalankan ping -c5 www.github.com

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar27.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar28.png)

Akhirnya, mari kita lepaskan shell kita dari kontainer, dengan menjalankan exit.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar29.png)

Langkah 4: Konfigurasikan NAT untuk konektivitas eksternal
----------------------------------------------------------

Mulai wadah baru berdasarkan gambar NGINX resmi dengan menjalankan docker run --name web1 -d -p 8080:80 nginx.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar30.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar31.png)

Tinjau status kontainer dan pemetaan port dengan menjalankan docker ps

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar32.png)

Jika karena alasan tertentu Anda tidak dapat membuka sesi dari web broswer, Anda dapat terhubung dari host Docker Anda menggunakan perintah curl 127.0.0.1:8080.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar33.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar34.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar35.png)

Bagian 3 - Overlay Networking
-----------------------------

Langkah 1: Dasar-Dasarnya

Jalnakan perintah Run docker swarm init --advertise-addr $(hostname -i).

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar36.png)

Jalankan node docker ls untuk memverifikasi bahwa kedua node adalah bagian dari Swarm.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar37.png)

Langkah 2: Buat jaringan overlay

Buat jaringan overlay baru yang disebut "overnet" dengan menjalankan docker network create -d overlay overnet.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar38.png)

Gunakan perintah docker network ls untuk memverifikasi bahwa jaringan berhasil dibuat.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar39.png)

Jalankan perintah docker network ls yang sama dari terminal kedua.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar40.png)

Gunakan jaringan  docker network inspect <network>  untuk melihat informasi lebih rinci tentang jaringan "overnet". Anda perlu menjalankan perintah ini dari terminal pertama.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar41.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar42.png)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar43.png)

Langkah 3: Buat layanan

Jalankan perintah berikut dari terminal pertama untuk membuat layanan baru bernama myservice pada jaringan overnet dengan dua tugas / replika.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar44.png)

Verifikasi bahwa layanan dibuat dan kedua replika sudah aktif dengan menjalankan docker service ls.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar45.png)

Pastikan bahwa satu tugas (replika) berjalan di masing-masing dari dua node di Swarm dengan menjalankan docker service ps myservice

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar46.png)

Sekarang simpul kedua menjalankan tugas pada jaringan "overnet", ia akan dapat melihat jaringan "overnet". 
Ayo lari docker network ls dari terminal kedua untuk memverifikasi ini.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-10/gambar47.png)














































