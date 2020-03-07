# tekn-basis-data
# Latihan pertama Tentang Hidupkan server Redis
Redis termasuk dalam paket resmi repositori Ubuntu. Namun, untuk mengakses dan menginstallnya, Anda perlu masuk ke server VPS melalui SSH. Setelah berhasil masuk ke server, Anda siap untuk menginstal Redis Ubuntu:
Update Cache APT Repository
Untuk menginstal Redis, Anda perlu mengupdate cache repositori APT Ubuntu Anda. Anda dapat melakukannya dengan command:
Kemudian user menginstal python dengan source codenya sudo apt install python-pip.

![Screenshot (2)](2.png)

![Screenshot (3)](3.png)

Sekarang, Anda dapat memasukkan beberapa shell, yang mana dapat menghubungkan kembali dengan  perintah Python redis dan perintah redis biasa dengan  menginstall redis-py.Tekan y dan enter untuk melanjutkan.
sudo apt install redis Didalam dokumen connect.py user menginputkan query seperti pada gambar dibawah agar saat mengecek Untuk memastikan apakah Redis telah terinstal koneksi antara redis dan pyton dan terhubung maka akan menampilkan “Connection to redis jas beend established” jika tidak terhubung maka akan menampilkan “Cannot connection to redis”.

![Screenshot (5)](5.png)
 
Menginstal Redis pada Ubuntu cukup mudah.jika sudah terhubung dengan redisnya dan pyton Kemudian user mengakses  dan masuk pada python, python siap dijalankan. 
dengan pertemuan yang pertama dapat masukan user dapat menjelaskan dan melakukan penginstalan redis pada terminal linux, disini user langsung mengakses dan masuk pada redis pada terminal.

# Latihan Kedua tentang Kerjakan Materi dan Penjelasan 2, 3 dan 4

STRING Pada perintah redis dapat mengatur nilai string, user menggunakan yang berikut dari redis-cli

![Screenshot (34)](34.png)

Coba dapatkan "mykey", yang diset menggunakan redis-cli dari Python. Output menampilkan hasil yang sama pada redis dimana python dapat berkomunikasi dengan benar dengan redis-server. merupakan redis untuk menggunakan redis-cli dapat dibaca menggunakan Python.

![Screenshot (6)](6.png)

Dapat mengatur nilai ke Redis dari Python shell.

![Screenshot (7)](7.png)

Dapat di lihat dari redis-cli apakah kunci ini disetel dengan benar.

![Screenshot (8)](8.png)

INCR dan INCRBY Redis juga menyediakan incr dan incrby pada nilai integer. Disini user akan mencoba menetapkan nilai integer setara redis-py dari Redis 'incr adalah ntuk Menampilkan untuk memverifikasi bahwa num telah bertambah.

![Screenshot (9)](9.png)

![Screenshot (10)](10.png)

![Screenshot (10)](10.png)

![Screenshot (11)](11.png)

![Screenshot (12)](12.png)

User untuk memastikan dengan mengecek menggunakan redis-cli.


![Screenshot (13)](13.png)

Python dengan incrby

![Screenshot (14)](14.png)

User untuk memastikan dengan mengecek lagi menggunakan redis-cli.

![Screenshot (15)](15.png)

Dapat dilihat dengan EXISTS

![Screenshot (16)](16.png)

DEL Saat kunci dapat  dihapus pada python, maka kita akan mendapatkan "nihil" dan "Tidak Ada" jika Anda mencoba mengambilnya pada redis selanjutnya untuk EXPIRE Tandai key second_num untuk kedaluwarsa setelah 10 detik

![Screenshot (17)](17.png)

![Screenshot (18)](18.png)

EXPIRE

![Screenshot (19)](19.png)

REDIS LISTS Redis lpush sama dengan menggunakan Python

![Screenshot (20)](20.png)

User ini dapat memastikan dan mengecek atau verifikasi bahwa list dibuat diredis

![Screenshot (21)](21.png)

kemudian menambahkan beberapa nilai ke list


![Screenshot (22)](22.png)

Periksa daftar baru dari redis-cli

![Screenshot (23)](23.png)

lihatlah dan periksalah daftar baru dari Python

![Screenshot (24)](24.png)

lanjut dengan rpush

![Screenshot (25)](25.png)

Periksa elemen yang didorong ke kanan

![Screenshot (35)](35.png)

REDIS HASHES hmset memungkinkan penyimpanan kamus sebagai nilai. Ini sama seperti pada redis docs.

![Screenshot (36)](36.png)

redis-py cara mencapai hal yang sama dapat Memastikan yang diinput pada python ini menggunakan redis-cli

![Screenshot (37)](37.png)

Menampilkan ini menggunakan redis-py

![Screenshot (38)](38.png)

Materi dan Penjelasan 3
Materi dan Penjelasan 4 Pada materi dan penjelasan dibagian 3 yaitu menulis sebuah program dengan python yang membutuhkan lima langkah dasar yaitu: 
-impor redis tentukan informasi koneksi untuk redis, membuat objek koneksi redis, mengatur pesan ke redis, mengambil pesan redis dan menampilkan pesan tersebut. 
Yang Pertama- tama pada shell unix python, disini user membuat dokumen baru dengan nama python3.py yang didalamnya akan berisi skrip untuk mengimplementasikan lima langkah tersebut seperti dibawah ini:

![Screenshot (27)](27.png)

Dari kode ini, user dapat memodifikasi kode tersebut menggunakan metode set dan get untuk menggunggah data yang berbeda. Dari program ini kita dapat bereksperimen dengan beberapa tipe data redis lain yang ditautkan diatas.