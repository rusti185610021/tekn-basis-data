# tekn-basis-data
# Latihan 1 (Aktifkan MongoDB Server)
# Install
Install MongoDB seperti halnya aplikasi biasa, dan secara default akan tersimpan di C:\Program and Files\mongodb. Kita bisa mengubah lokasi installnya dengan memilih custom pada saat instalasi. Asumsi MongoDB terinstall di C:\mongodb, dan binary nya berada di folder C:\mongodb\bin.

![Screenshot (50)](Screenshot(50).png)

Setting MongoDB environment
MongoDB membutuhkan folder data untuk menyimpan database, buatlah folder dengan nama dan lokasi c:\data\db
Daftarkan path folder “data” nya menggunakan --dbpath ke mongod.exe :

# Start Server MongoDB
Untuk menjalankan daemon/service MongoDB jalankan peritah ini dengan membuka Command Prompt :

![Screenshot (51)](Screenshot(51).png)

# Latihan 2 (Install Python)
Mendownload Executable Installer Python
Unduh instalasi Python yang berbentuk executable di https://www.python.org/downloads/windows/. Pilih versi terbaru yang paling stabil yaitu link paling atas.

kemudian sesuaikan versi arsitektur sistem operasi Windows yang digunakan. Pilih x86-64 untuk arsitektur sistem operasi 64bit atau pilih x86 untuk arsitektur sistem operasi 32bit.
![Screenshot (53)](Screenshot(53).png)

Buka file installer yang telah di download

![Screenshot (54)](Screenshot(54).png)

Centang Install launcher for all user untuk mengaktifkan python pada semua user Windows dan centang Python 3.6 to PATH untuk menambah path command Python. Kemudian klik Install Now. Klik Yes saat muncul notifikasi User Account Control.

![Screenshot (45)](Screenshot(45).png)

![Screenshot (46)](Screenshot(46).png)

Tunggu proses install hingga selesai.

Opsi “Disable path length limit”
Disini, anda dapat mengaktifkan atau menonaktifkan batasan lintasan direktori Python. Untuk pengguna Linux batasan ini tidak mempunyai pengaruh yang besar, karena Linux menyimpan python pada direktori yang pendek. Berbeda halnya dengan Windows, yang menyimpan direktori lintasan agak jauh dari direktori utama partisi. Disarankan untuk menonaktifkan batasan ini dengan klik “Disable path length limit“.

![Screenshot (47)](Screenshot(47).png)

![Screenshot (48)](Screenshot(48).png)
Klik Yes saat muncul notifikasi User Account Control.
Klik Close untuk menutup installer Python.

Install Python berhasil

![Screenshot (48)](Screenshot(48).png)

Terdapat beberapa aplikasi yang dapat digunakan • Python IDLE Shell ; IDLE adalah kependekan dari Python’s Integrated Development and Learning Environment yang merupakan IDE standar Python. • Python 3.6 ; untuk membuka python melalui command prompt. • Python 3.6 Manual ; Panduan manual Python. • Python Module 3.6 Doc ; Panduan mengenai module pada Python. Disini user menggunakan IDLE Shell lalu melakukan pengujian dengan mencetak kalimat “hello world”.

# Latihan 3 (Install Visual Code serta Extention untuk Python)
Sebelumnya user sudah mempunyai aplikasi visual studio code. Disini user hanya tinggal menginstal extension untuk python saja.

![Screenshot (52)](Screenshot(52).png)

![Screenshot (53)](Screenshot(53).png)

# Latihan 4 (Kerjakan Instalasi PyMongo)
Untuk menginstalasi PyMongo, disini user menggunakan pip dimana yang dimaksud dengan pip yaitu penginstal paket untuk Python yang dapat digunakan untuk menginstal paket dari Indeks Paket Python dan indeks lainnya. Untuk meningkatkan menggunakan pip

![Screenshot (55)](Screenshot(55).png)

untuk menginstal pymongo di semua platform

![Screenshot (57)](Screenshot(57).png)

# Latihan 5 (Kerjakan Tutorial Materi dan Penjelasan nomor 4 diatas
Berikut ini beberapa tutorial yang user kerjakan didalam modul pada pertemuan 3. Pertama-tama sebelum mengerjakan tutorial user sudah menginstal dan berada di tampilan command promp pyton. n

![Screenshot (58)](Screenshot(58).png)

Membuat Koneksi dengan MongoClient Pada baris pertama yaitu membuat MongoClient ke instance mongod yang sedang berjalan. Kode berikut akan menghubungkan pada host dan port secara default. 

![Screenshot (59)](Screenshot(59).png)

Dibawah ini akan menentukan host dan port secara eksplisit dengan menggunakan format URL agar menghubungkan ke server database mongoclient.

![Screenshot (60)](Screenshot(60).png)
Membuat dan memperoleh basis data dari python Saat terkoneksi dengan mongodb, agar dapat mengakses database menggunakan atribut pada instance mongoclient akan menampilkan database yang disudah dibuat pada python.mengecek keberhasilan dalam membuat database menggunakan python, user menggunakan command prompt mongodb untuk menampilkan database yang dibuat dengan kode show dbs.
Membuat dan memperoleh collection atau tabel dari python Collection merupakan dokumen/data yang disimpan dalam database mongodb yang dapat dianggap setara dengan tabel dalam database relasional. Untuk membuat collection di pymongo yaitu dengan kode pada gambar berikut


![Screenshot (61)](Screenshot(61).png)

![Screenshot (62)](Screenshot(62).png)

![Screenshot (63)](Screenshot(63).png)

![Screenshot (64)](Screenshot(64).png)
Dokumen Dokumen dalam monggodb dibawah menggunakan style JSON yang berisi beberapa field yang didalamnya memposting nama, teks, tag dan waktu yang akan diisi pada collection atau tabel post.

![Screenshot (65)](Screenshot(65).png)
Menyisipkan dokumen untuk menyisipkan dokumen ke dalam collection, dibaris pertama terdapat collection posts yang berisi data base yang sudah dibuatkan sebelumya. Kemudian pada baris kedua dokumen membuat post_id yang berisi metode insert_one dengan collection post. Kemudian, ditambahkan inserted_id dimana secara otomatis ditambahkan jika dokumen tersebut belum mengandung kunci "_id". dibaris ketiga user memanggil kembali post_id yang berarti secara otomatis ditambahkan objekId agar menghasilkan nilai unik objekId yang bertipe heksadesimal.Setelah memasukkan dokumen pertama, koleksi posts sebenarnya telah dibuat di server. user hanya dapat memverifikasi ini dengan men-list semua koleksi yang ada di database
Memperoleh dokumen tunggal menggunakan find_one Metode ini menampilkan dokumen yang teratas atau paling awal dari collection entry.

![Screenshot (66)](Screenshot(66).png)
![Screenshot (67)](Screenshot(67).png)
![Screenshot (68)](Screenshot(68).png)

Cara yang kedua yaitu menampilkan dokumen berdasarkan ekspresi dokumen yang dengan penulis “Mike”.
![Screenshot (69)](Screenshot(69).png)

selanjutnya cara ketiga yaitu menampilkan dokumen berdasarkan ekspresi dokumen yang dengan penulis “Eliot”, namun pada didalam collection tidak ada dokumen penulis dengan nama “Eliot”.
Kemudian di baris ketiga yaitu menampilkan dokumen berdasarkan ekspresi dokumen yang sesuai dengan id pada gambar dibawah.Untuk bahwa merubah nama post_id menjadi string. Kemudian di baris kedua akan menampilkan datanya menjadi string. Namun didalam collection tidak ada dokumen post_id yang sebagai string.
Masukan banyak data Disini menampilkan kode untuk memasukkan beberapa banyak data. Dimana akan memasukkan setiap dokumen dalam daftar, hanya mengirimkan satu perintah ke server. ada beberapa yang perlu diperhatikan dalam kode dibawah yaitu pada insert_many yang dapat mengembalikan dua atau lebih instance ObjectId untuk setiap dokumen yang dimasukkan. Dan yang kedua yaitu new_posts memiliki bentuk yang berbeda dimana tidak ada field “tags” namun diganti dengan field “title”. Perbedaan inilah yang dimaksud bahwa MongoDB atau noSQL bebas skema.

![Screenshot (69)](Screenshot(69).png)
![Screenshot (71)](Screenshot(71).png)
masuk di bagian Query untuk lebih dari satu dokumen Disini akan menampilkan lebih dari satu dokumen yang akan mengulangi setiap dokumen dalam setiap post.
![Screenshot (73)](Screenshot(73).png)
![Screenshot (74)](Screenshot(74).png)
Query keduan akan menampilkan dokumen yang berdasarkan field author dengan nama “Mike”.
![Screenshot (75)](Screenshot(75).png)
Kode pertama menghitung keseluruhan data dokumen pada colletion posts.
kedua menghitung banyak data dokumen pada collection posts dengan permintaan tertentu yaitu dengan field author : “Mike”.
![Screenshot (76)](Screenshot(76).png)
![Screenshot (77)](Screenshot(77).png)
Lebar query  baris pertama terdapat field d yang berisi rentang waktu yang sudah ditentukan dan di kode baris yang kedua perintah untuk menampilkan dokumen dengan rentang waktu kurang dari rank yang ada di field d yang di sortir berdasarkan author.
Kemudian masuk dibagian Index Disini akan membuat index pada collection profiles yang akan diurutkan nilai user_id secara terkecil ke terbesar (ascending) dan dengan id yang unik.
kode pada gambar dibawah mengatur beberapa dokumen pada field user_profiles.