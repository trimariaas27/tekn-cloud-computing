LATIHAN 
=======

Melakukan Pengecekan Version Docker Compose 

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar1.png)

Melakukan Migrate 

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar2.png)

Perintah untuk melakukan pengecekkan kontainer yang sedang aktif

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar3.png)

Proses Ping 127.0.0.1

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar4.png)

Langkah 4: Bangun dan jalankan aplikasi Anda dengan Compose

A. Dari direktori proyek Anda, mulai aplikasi Anda dengan menjalankan docker-compose up.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar5.png)

B. Masukkan http: // localhost: 5000 / di browser untuk melihat aplikasi berjalan.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar6.png)

C. Perbarui halaman. Jumlahnya harus bertambah.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar7.png)

D. Beralih ke jendela terminal lain, dan ketik docker image ls untuk mencantumkan gambar lokal. Daftar gambar pada titik ini harus kembali redisdan web.

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar8.png)

Langkah 8:  percobaan dengan beberapa perintah lain

A. -dflag (untuk mode "terlepas") ke docker-compose updan gunakan docker-compose ps untuk melihat apa yang sedang berjalan:

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar9.png)

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar10.png)

B. docker-compose run perintah memungkinkan Anda untuk menjalankan satu-off perintah untuk layanan Anda. Misalnya, untuk melihat variabel lingkungan apa yang tersedia untuk web layanan:

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar11.png)

C. Jika Anda mulai menulis dengan docker-compose up -d, hentikan layanan Anda setelah selesai menggunakannya:

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar12.png)

D. dengan down perintah. Lulus --volumes untuk juga menghapus volume data yang digunakan oleh wadah Redis:

![alt text](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-08/gambar13.png)

  