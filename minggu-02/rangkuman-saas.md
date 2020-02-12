Apa perbedaan antara IaaS, SaaS, dan Paas?
=========================================

IaaS (Infrastruktur as a Service)
IaaS mengacu pada sumber daya infrastruktur berbasis cloud yang memanfaatkan teknologi virtualisasi untuk membantu organisasi membangun dan mengelola server, jaringan, sistem operasi, dan penyimpanan data. Pelanggan dapat mengakses dan menyimpan data pada server melalui dashboard atau API (application programming interface). Seiring dengan bertumbuhnya perusahaan, IaaS membantu perusahaan membangun dan mengelola data mereka. Infrastruktur cloud IaaS menawarkan tingkat kontrol dan kekuatan terbesar atas perangkat lunak dan perangkat keras perusahaan dan administrator. IaaS juga bertanggung jawab untuk memastikan keamanan dan pengoperasian sistem, untuk menghindari pemadaman di bagian-bagian penting operasional perusahaan. Contoh Dari IaaS sebagai berikut :
* Amazon Web Services (AWS)
* Microsoft Azure

SaaS (Software as a Service)
SaaS mengacu pada perangkat lunak berbasis cloud yang di-host online oleh perusahaan, dan bisa dibeli secara berlangganan dan dikirimkan melalui internet. Produk SaaS adalah salah satu layanan komputasi awan yang paling sering digunakan oleh perusahaan untuk membangun dan mengembangkan bisnis mereka, karena mudah digunakan dan dikelola, dan sangat skalabel, karena tidak perlu diunduh dan dipasang di masing-masing perangkat untuk menyebarkannya ke seluruh tim atau perusahaan. Ini sangat berguna bagi tim yang berkerja dengan terpisahkan ruang dan jarak. Contoh Dari SaaS sebagai berikut :
* Jira
* Dropbox

PaaS (Platform as a Service)
PaaS mengacu pada layanan platform berbasis cloud yang memberikan kerangka kerja yang dapat digunakan oleh pengembang untuk membuat aplikasi kustom. Dengan PaaS, aplikasi kustom bisa dibangun secara online tanpa harus berurusan dengan penyajian data, penyimpanan, dan manajemen. PaaS menyediakan platform online yang dapat diakses oleh berbagai pengembang untuk membuat perangkat lunak yang disampaikan melalui internet. Contoh Dari PaaS sebagai berikut :
* Google App Engine
* Open Shift

Arsitektur Platform SAAS (Perangkat Lunak sebagai Layanan)
==========================================================

Perangkat lunak sebagai layanan adalah model lisensi dan pengiriman perangkat lunak di mana perangkat lunak dilisensikan berdasarkan berlangganan dan di-host secara terpusat. Pengguna dapat mengaksesnya dengan bantuan browser web.

SaaS adalah model pengiriman umum untuk banyak aplikasi bisnis, termasuk perangkat lunak perkantoran dan pesan, perangkat lunak manajemen, virtualisasi dll. Ini adalah bagian dari nomenklatur komputasi awan, bersama dengan infrastruktur sebagai layanan (IaaS), platform sebagai layanan (PaaS) , desktop sebagai layanan (DaaS).

Penyedia SaaS menyimpan aplikasi dan data secara terpusat - tambalan penyebaran. Mereka meningkatkan ke aplikasi secara transparan, memberikan akses ke pengguna akhir melalui Internet. Banyak vendor menyediakan API yang digunakan pengembang untuk membuat aplikasi komposit. Ini berisi berbagai mekanisme keamanan untuk keamanan data selama transmisi dan penyimpanan.

![png](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-02/gambar1.png) 

Ada dua varietas utama SaaS:

SaaS Vertikal
Perangkat Lunak yang menjawab kebutuhan industri tertentu (mis. Perangkat lunak untuk kesehatan, pertanian, real estat, industri keuangan)
SaaS Horisontal
Produk-produk yang berfokus pada kategori perangkat lunak (pemasaran, penjualan, alat pengembang, SDM) tetapi agnostik industri.

![png](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-02/gambar2.png)

Arsitektur Platform SAAS (Perangkat Lunak sebagai Layanan)
==========================================================

Mengapa Menggunakan Arsitektur SaaS?

![png](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-02/gambar3.jpg)

Seperti yang disebutkan dalam pendahuluan, perangkat lunak telah didistribusikan kepada pelanggan dalam berbagai saluran selama beberapa dekade terakhir. Saluran distribusi yang lebih baru dalam Perangkat Lunak sebagai Layanan (atau SaaS).

Cara membangun aplikasi SaaS berbasis cloud
============================================

* Memilih Bahasa Pemrograman Yang Dikuasai
* Memilih MongoDB Sebagai Database. Dikarenakan MongoDb adalah database berorientasi dokumen yang memberikan kinerja tinggi.
* Mengatur MongoDb untuk aplikasi SaaS kita.
* Menggunakan Sistem Antrian RabbitMQ.
* Membangun Aplikasi Web yang skalabel menggunakan Amazon Web Service. AWS memnungkinkan untuk meng-host dan  menjalankan aplikasi web serta melakukan pekerjaan batch berkinerja tinggi. Dengan Elastic Compute Cloud (EC2) AWS menyediakan server virtual yang dapat diskalakan untuk setiap bisnis.

![png](https://github.com/trimariaas27/tekn-cloud-computing/blob/master/minggu-02/gambar4.jpg)










