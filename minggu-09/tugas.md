Docker for Beginners - Linux
============================

Clone Repo GitHub Lab
---------------------

Gunakan perintah berikut untuk mengkloning repo lab dari GitHub :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_1.PNG)

Tugas 1: Jalankan beberapa wadah Docker sederhana 
=================================================

Jalankan satu tugas dalam wadah Alpine Linux
--------------------------------------------

Jalankan perintah berikut di konsol Linux :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_2.PNG)

Jalankan perintah docker container ls --all untuk melihat wadah Alpine Linux Anda :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_3.PNG)

Jalankan wadah Ubuntu interaktif
--------------------------------

Jalankan wadah Docker dan akses :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_4.PNG)

Jalankan perintah berikut dalam wadah Alpine Linux :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_5.PNG)

ls /akan mencantumkan isi direktur root dalam wadah, ps auxakan menunjukkan proses yang berjalan dalam wadah, 
cat /etc/issueakan menunjukkan distro Linux mana wadah berjalan.

Jalankan perintah exit untuk meninggalkan sesi shell :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_6.PNG)

Periksa versi host VM :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_7.PNG)

Jalankan latar belakang wadah MySQL
-----------------------------------

Jalankan wadah MySQL baru dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_8.PNG)

--detach akan menjalankan wadah di latar belakang.
--nameakan menamainya mydb .
-e akan menggunakan variabel untuk menentukan kata sandi root.

Melihat Daftar wadah yang sedang berjalan :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_9.PNG)

Memeriksa apa yang terjadi di wadah Anda dengan menggunakan beberapa perintah Docker Yaitu docker container logs :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_10.PNG)

Melihat proses yang berjalan di dalam wadah :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_11.PNG)

Melihat Daftar versi MySQL menggunakan docker container exec :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_12.PNG)

Menggunakan docker container exec untuk terhubung ke proses shell baru di dalam wadah yang sudah berjalan :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_13.PNG)

Periksa nomor versi dengan menjalankan perintah yang sama lagi dan gunakan perintah exit untuk meninggalkan sesi shell :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_14.PNG)

Gunakan Perintah Exit untuk keluar dari cell :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_15.PNG)

Tugas 2: Paket dan menjalankan aplikasi khusus menggunakan Docker
=================================================================

Pastikan Anda berada di linux_tweet_app direktori dengan menjalankan perintah :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_16.PNG)

Tampilkan konten Dockerfile dengan menjalankan perintah :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_17.PNG)

FROM menentukan gambar dasar untuk digunakan sebagai titik awal untuk gambar baru yang Anda buat ini. Untuk contoh ini kita mulai dari nginx:latest.
COPY menyalin file dari host Docker ke dalam gambar, di lokasi yang diketahui. Dalam contoh ini, COPY digunakan untuk menyalin dua file ke dalam gambar: index.html. dan grafik yang akan digunakan di halaman web.
EXPOSE dokumen yang port aplikasi gunakan.
CMD menentukan perintah apa yang harus dijalankan ketika sebuah wadah dimulai dari gambar.

Jalankan Perintah Export DockerId diikuti id docker masing-masing sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_18.PNG)

Gunakan perintah build image docker untuk membuat image Docker baru menggunakan instruksi di Dockerfile :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_19.PNG)
![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_19a.PNG)

Gunakan perintah container run untuk container baru dari gambar yang dibuat :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_20.PNG)

Menjalkan situs web yang seharusnya berjalan dengan menjalankan perintah sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_21.PNG)

Setelah Anda mengakses situs web Anda, matikan dan hapus dengan menggunakan perintah sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_22.PNG)

Tugas 3: Memodifikasi Situs Web Yang Sedang Berjalan 
====================================================

Mulai aplikasi web dengan bind mount
-----------------------------------------

Pastikan untuk menjalankan perintah ini dari dalam direktori linux_tweet_app pada host Docker Anda dengan menggunakan perintah sebagai berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_23.PNG)

Ubah situs web yang berjalan
----------------------------

Salin index.html baru ke dalam wadah dengan menggunakan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_24.PNG)

Hentikan dan hapus wadah yang sedang berjalan dengan menjalankan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_25.PNG)

Jalankan kembali versi saat ini tanpa bind mount dengan menggunakan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_26.PNG)

Perhatikan situs web kembali ke versi aslinya dengan menggunakan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_27.PNG)

Berhenti dan lepaskan wadah saat ini dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_28.PNG)

Perbaharui Gambar
-----------------

Menjalankan perintah build image docker lain akan membuat image baru dengan index.html yang diperbarui dengan menggunakan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_29.PNG)

Melihat Gambar Pada Sistem Dengan Menggunakan Perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_30.PNG)

Uji Versi Baru
--------------

Jalankan container baru dari versi gambar yang baru dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_31.PNG)

Periksa versi baru situs web (Anda mungkin perlu menyegarkan  untuk mendapatkan versi baru untuk dimuat) :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_32.PNG)

Jalankan container baru, kali ini dari versi lama gambar dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_33.PNG)

Dorong gambar Anda ke Docker Hub
--------------------------------

Daftar gambar pada host Docker Anda dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_34.PNG)

Sebelum Anda dapat mendorong gambar Anda, Anda harus masuk ke Docker Hub dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_35.PNG)

Dorong versi 1.0 aplikasi web Anda menggunakan push gambar dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_36.PNG)

Sekarang dorong versi 2.0. dengan perintah berikut :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_37.PNG)

Anda dapat menjelajah ke  https://hub.docker.com/r/<your docker id>/ / dan melihat gambar Docker yang baru Anda dorong. Ini adalah repositori publik, sehingga siapa pun dapat menarik gambar - Anda bahkan tidak memerlukan ID Docker untuk menarik gambar publik. Docker Hub juga mendukung repositori pribadi :

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-09/Capture_38.PNG)








