# pert4-6
Nama	NIM	Kelas	Matkul
Bayu Tri Wicaksono	312310407	TI.23.A4	Pemograman Web 1
membuat tabel user login di mysql image

Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori app/Models dengan nama UserModel.php image

Buat Controller baru dengan nama User.php pada direktori app/Controllers. Kemudian tambahkan method index() untuk menampilkan daftar user, dan method login() untuk proses login. image image

Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php. image image image image

Membuat Database Seeder Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut: image

Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori /app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut: image

Selanjutnya buka kembali CLI dan ketik perintah berikut: image

Uji Coba Login Selanjutnya buka url http://localhost:8080/user/login seperti berikut: image

Menambahkan Auth Filter Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori app/Filters. image

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut: image

Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya. image
refresh kembali maka akan ke menu login

Fungsi Logout Tambahkan method logout pada Controller User seperti berikut: image
pertemuan 5

Membuat Pagination Pagination merupakan proses yang digunakan untuk membatasi tampilan yang panjang dari data yang banyak pada sebuah website. Fungsi pagination adalah memecah tampilan menjadi beberapa halaman tergantung banyaknya data yang akan ditampilkan pada setiap halaman. Pada Codeigniter 4, fungsi pagination sudah tersedia pada Library sehingga cukup mudah menggunakannya. Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi kode pada method admin_index seperti berikut. image

Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut dibawah deklarasi tabel data. image Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat hasilnya. image

Membuat Pencarian Pencarian data digunakan untuk memfilter data. Untuk membuat pencarian data, buka kembali Controller Artikel, pada method admin_index ubah kodenya seperti berikut image

Kemudian buka kembali file views/artikel/admin_index.php dan tambahkan form pencarian sebelum deklarasi tabel seperti berikut: image Dan pada link pager ubah seperti berikut. image

Selanjutnya ujicoba dengan membuka kembali halaman admin artikel, masukkan kata kunci tertentu pada form pencarian. image

pertemuan 6

Upload Gambar pada Artikel Menambahkan fungsi unggah gambar pada tambah artikel. Buka kembali Controller Artikel pada project sebelumnya, sesuaikan kode pada method add seperti berikut: image

Kemudian pada file views/artikel/form_add.php tambahkan field input file seperti berikut. image Dan sesuaikan tag form dengan menambahkan ecrypt type seperti berikut. image

Ujicoba file upload dengan mengakses menu tambah artikel. image

About
No description, website, or topics provided.
Resources
 Readme
 Activity
Stars
 0 stars
Watchers
 1 watching
Forks
 0 forks
Report repository
Releases
No releases published
Packages
No packages published
Footer
© 2025 GitH
