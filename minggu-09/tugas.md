Docker for Beginners - Linux
============================

Clone Repo GitHub Lab
---------------------

Gunakan perintah berikut untuk mengkloning repo lab dari GitHub :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_1.PNG)

Tugas 1: Jalankan beberapa wadah Docker sederhana 
=================================================

Jalankan satu tugas dalam wadah Alpine Linux :

Jalankan perintah berikut di konsol Linux

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_2.PNG)

Jalankan perintah docker container ls --all untuk melihat wadah Alpine Linux Anda :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_3.PNG)

Jalankan wadah Ubuntu interaktif
--------------------------------

Jalankan wadah Docker dan akses :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_4.PNG)

Jalankan perintah berikut dalam wadah Alpine Linux :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_5.PNG)

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_6.PNG)

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_7.PNG)

ls /akan mencantumkan isi direktur root dalam wadah, ps auxakan menunjukkan proses yang berjalan dalam wadah, 
cat /etc/issueakan menunjukkan distro Linux mana wadah berjalan.

Jalankan perintah exit untuk meninggalkan sesi shell :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_8.PNG)

Periksa versi host VM :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_9.PNG)

Jalankan latar belakang wadah MySQL
-----------------------------------

Jalankan wadah MySQL baru dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_10a.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_10b.PNG)

--detach akan menjalankan wadah di latar belakang.
--nameakan menamainya mydb .
-e akan menggunakan variabel untuk menentukan kata sandi root.

Melihat Daftar wadah yang sedang berjalan :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_11.PNG)

Memeriksa apa yang terjadi di wadah Anda dengan menggunakan beberapa perintah Docker Yaitu docker container logs :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_12.PNG)

Melihat proses yang berjalan di dalam wadah :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_13.PNG)

Melihat Daftar versi MySQL menggunakan docker container exec :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_14.PNG)

Menggunakan docker container exec untuk terhubung ke proses shell baru di dalam wadah yang sudah berjalan :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_15a.PNG)

Periksa nomor versi dengan menjalankan perintah yang sama lagi dan gunakan perintah exit untuk meninggalkan sesi shell :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_15.PNG)

Tugas 2: Paket dan menjalankan aplikasi khusus menggunakan Docker
=================================================================

Pastikan Anda berada di linux_tweet_app direktori :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_16.PNG)

Tampilkan konten Dockerfile :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_17.PNG)

FROM menentukan gambar dasar untuk digunakan sebagai titik awal untuk gambar baru yang Anda buat ini. Untuk contoh ini kita mulai dari nginx:latest.
COPY menyalin file dari host Docker ke dalam gambar, di lokasi yang diketahui. Dalam contoh ini, COPY digunakan untuk menyalin dua file ke dalam gambar: index.html. dan grafik yang akan digunakan di halaman web.
EXPOSE dokumen yang port aplikasi gunakan.
CMD menentukan perintah apa yang harus dijalankan ketika sebuah wadah dimulai dari gambar.






