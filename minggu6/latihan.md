# tekn-basis-data
# latihan Install Apache Cassandra hinggal bisa dijalankan server dan cqlsh
Cara pertma menginstal OpenJDK yang telah saya download pada link github praktikum atau bisa diakses di link OpenJDK. Langkah penginstalan ada dibawah ini. setelah  program sudah selesai didownload, open file instalasi OpenJDK kemudian klik next.

![Screenshot (1)](1.png)

Kemudian pada END-USER LICENSE AGREEENT klik checkbox/centang pada I accept the terms in the license Agreement.
pada tab CUSTOM SETUP kita menentukan simpanan directori yang akan disimpan saat diinstalasi. Jika sudah klik tombol next.
![Screenshot (2)](2.png)

pada tab CUSTOM SETUP kita menentukan simpanan directori yang akan disimpan saat diinstalasi. Jika sudah klik tombol next

![Screenshot (3)](3.png)

klik supaya dapat dilanjutkan

![Screenshot (4)](4.png)

setelah itu tunggu sampai selesai di proses untuk OpenJDK.

![Screenshot (5)](5.png)

Dapat memastikan kalau aplikasi selesai di install buka cmd lalu klik kode  java.exe -version.

![Screenshot (6)](6.png)

selajutnya kalau sudah terinstaal buka Environment pada Control panel /Pilih Environment Variable

![Screenshot (26)](26.png)

Copykan alamat tempat folder penginstallan jdk dengan cara : Computer > local Disk (c) > program files > java > folder jdk > bin > java Setelah itu klik kanan pada Computer > Properties > Advanced System Settings kemudian Pilih Environment Variable.
Cari variable Path dan pastekan  lokasi penyimpanan folder jdk pada variable value lalu klik ok

![Screenshot (27)](27.png)

Langkah berikutnya user menginstall python. 


![Screenshot (9)](9.png)

Pada menu CUSTOMIZE PYTHON user memilih Will be installed on local hard drive, selanjutnya ikuti petunjuk sampai proses instalasi selesai.lanjut klik next dapat melanjutkan install.

![Screenshot (10)](10.png)

Tunggu sampai selesai  proses.

![Screenshot (11)](11.png)

selanjutnya klik finish otomatis aplikasi pyton sudah terinstall,lanjut langkah selanjutnya.

![Screenshot (12)](12.png)

Langkah ketiga selesai mendownload Apache Cassandra versi 3.11.6, setelah selesai didownload, unzip dan tempatkan pada direktori “C:\Program Files\apache-cassandra-3.11.6-bin”.

![Screenshot (13)](13.png)

kemudiansudah dipindahkan di direktori yang ditentukan, selanjutnya buka Command promp dan masuk ke directori yang ditentukan kemudian ketik Cassandra yang hasilnya seperti ditunjukkan di bawah ini.

![Screenshot (28)](28.png)

Selanjutnya kita lanjut lagi setting CASSANDRA_HOME untuk nama variabel nya dan directori nya arahkan ke C:\cassandra\bin , tampilannya seperti ini

![Screenshot (15)](15.png)

lalu sama seperti langkah sebelumya, dibuat juga path pada system variable dengan mengklik path pada system variabel. Klik new dan browse directory yang sama dengan yang kita buat saat membuat variabel name cassandra_home yaitu di C:\cassandra\bin.

![Screenshot (16)](16.png)

Menjalankan Apache Cassandra
Cara paling dasar untuk berinteraksi dengan Cassandra adalah menggunakan shell CQL yaitu cqlsh. Anda dapat membuat basis data dan tabel, menambah data baru, mencari, mengubah dan menghapus data yang ada. dan masih banyak lagi yang lain.
Untuk menjalankan Cassandra, gunakan powershell atau command prompt.
Untuk memulai shell CQL, ketikkan cqlsh, tekan Enter.

![Screenshot (17)](17.png)

Shell siap menerima perintah CQL (Cassandra Query Language). Misalnya, dengan mengetikkan help akan tampil layar berikut.

![Screenshot (18)](18.png)

Selanjutnya kita coba membuat tabel di dalamnya. untuk langkah Pertama-tama buat namespace tempat data disimpan.

![Screenshot (19)](19.png)

