# tekn-basis-data
# Kerjakan A Practical Introduction to Cassandra Query Language. Sesuaikan dengan instalasi anda dan versi CQL terbaru yang anda gunakan.
Cassandra Query Language atau CQL adalah bahasa deklaratif yang memungkinkan pengguna untuk meminta Cassandra menggunakan bahasa yang mirip dengan SQL. CQL diperkenalkan di Cassandra versi 0.8 dan sekarang merupakan cara yang lebih disukai untuk mengambil data dari Cassandra. Sebelum pengenalan CQL, Thrift API berbasis RPC, adalah cara yang disukai untuk mengambil data dari Cassandra. Manfaat utama CQL adalah kesamaannya dengan SQL dan karenanya membantu menurunkan kurva pembelajaran Cassandra. CQL adalah SQL dikurangi bit yang rumit. Pikirkan CQL sebagai API sederhana di atas struktur penyimpanan internal Cassandra.
Dalam tugas ini kita mulai dengan membuat keyspace. Seperti yang disebutkan sebelumnya, keyspace mirip dengan skema / basis data di dunia RDBMS. Untuk membuat keyspace, jalankan CQL berikut. Perhatikan bagian “WITH REPLICATION” dari perintah.

![Screenshot (20)](20.png)

Selanjut Untuk membuat kolom, Anda harus menavigasi ke ruang kunci animal dengan bantuan "perintah USE". Perintah USE memungkinkan klien untuk terhubung ke keyspace tertentu sehingga semua perintah CQL lebih lanjut akan dieksekusi dalam konteks keyspace yang dipilih. Jalankan perintah ini akan membuka prompt cqlsh. Mari kita mulai dengan menciptakan ruang kunci. Seperti yang disebutkan sebelumnya, keyspace mirip dengan skema / basis data di dunia RDBMS.

![Screenshot (21)](21.png)

Perhatikan bagian “WITH REPLICATION” dari perintah. Ini menyatakan bahwa keyspace hewan harus menggunakan strategi replikasi sederhana dan hanya akan memiliki satu replika untuk semua data yang dimasukkan ke dalam keyspace. Ini bagus untuk tujuan demonstrasi tetapi bukan pilihan praktis untuk segala jenis pengujian atau lingkungan produksi.

Selanjutnya mari kita membuat keluarga kolom. Untuk membuat keluarga kolom, Anda harus menavigasi ke ruang kunci hewan dengan bantuan "perintah USE". Perintah USE memungkinkan klien untuk terhubung ke keyspace tertentu yaitu semua perintah CQL lebih lanjut akan dieksekusi dalam konteks keyspace yang dipilih. Jalankan perintah berikut di prompt cqlsh Anda untuk menghubungkan klien Anda saat ini ke animalkeyspace.

gunakan animalkeyspace;
Perhatikan Anda prompt cqlsh akan berubah dari hanya "cqlsh>" ke "cqlsh: animalkeyspace>" yang secara visual akan mengingatkan Anda tentang keyspace Anda saat ini terhubung.

Sekarang mari kita buat kolom keluarga / tabel untuk menampung data terkait monyet. Untuk mendefinisikan tabel, kita harus menggunakan perintah CREATE TABLE. Harap perhatikan kunci utama. Kunci utama terdiri dari dua bagian. mis. kunci partisi / baris dan kunci cluster. Kolom pertama dari kunci utama adalah kunci partisi Anda. Kolom yang tersisa digunakan untuk menentukan kunci cluster. Kunci partisi komposit, kunci partisi yang terdiri dari beberapa kolom, dapat didefinisikan dengan menggunakan seperangkat tanda kurung tambahan sebelum kolom pengelompokan. Kunci baris membantu mendistribusikan data di seluruh cluster sementara kunci cluster menentukan urutan data yang disimpan dalam satu baris. Jadi ketika mendesain tabel pikirkan kunci baris sebagai alat yang digunakan untuk menyebarkan data secara merata ke seluruh cluster, sedangkan kunci cluster membantu menentukan urutan data tersebut dalam satu baris. Patters kueri Anda akan sangat memengaruhi kunci cluster karena digunakan untuk mengurutkan data yang disimpan dalam satu baris. Perhatikan bahwa kunci cluster adalah opsional.

Mari kita membuat tabel Monkey dengan mengeksekusi perintah berikut di prompt cqlsh Anda

![Screenshot (22)](22.png)

Dalam tabel di atas kami telah memilih pengidentifikasi sebagai kunci partisi kami dan spesies sebagai kunci cluster.

![Screenshot (23)](23.png)


Seperti yang disebutkan dalam artikel sebelumnya, harus mencoba dan memvisualisasikan keluarga kolom Cassandra sebagai peta peta yang diurutkan yaitu Peta <rowkey, sortmap <columnkey, = "" columnvalue = "" >> >>). Data yang dimasukkan ke dalam tabel Monkey dapat divisualisasikan sebagai peta di bawah ini.

![Screenshot (24)](24.png)


![Screenshot (25)](25.png)

Perhatikan kunci partisi 5132b130ae7911e4ab270800200c9a66 adalah kunci baris dan kunci untuk peta luar kita. "Monyet Capuchin:" adalah kunci kluster kami dan entri pertama di peta yang diurutkan dalam. Entri pertama dari peta yang disortir tidak memiliki data apa pun karena kunci dan datanya sama. Entri peta selanjutnya membuat kunci dengan suffexing nama kolom ke kunci cluster. "Capuchin monkey: nickname" kunci adalah hasil dari kunci cluster + nama panggilan header kolom. Bagian data berisi data aktual untuk kolom.Gambar di atas ini secara visual menggambarkan keterkaitan antara baris CQL SSTable yang dihasilkan dan peta logis dari peta yang diurutkan