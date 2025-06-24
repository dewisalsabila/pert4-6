|Nama|NIM|Kelas|Matkul|
|----|---|-----|------|
|Dewi Salsabila|312310722|TI.23.A4|Pemograman Web 1|

1. membuat tabel user login di mysql
![image](https://github.com/user-attachments/assets/77bf533c-41c6-4fed-a1e1-e68c2cb7584d)

2. Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori
app/Models dengan nama UserModel.php
![image](https://github.com/user-attachments/assets/29d89ff6-9e1b-4beb-93d9-303496963ca0)

3. Buat Controller baru dengan nama User.php pada direktori app/Controllers. Kemudian
tambahkan method index() untuk menampilkan daftar user, dan method login() untuk proses
login.
![image](https://github.com/user-attachments/assets/100a9083-d5b9-4c30-9d3d-44c31fc4bf11)
![image](https://github.com/user-attachments/assets/6c26f7d9-eac0-46b2-9172-3917b499f0f5)

4. Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file baru
dengan nama login.php.
![image](https://github.com/user-attachments/assets/5a6aed90-e960-4c41-9f3e-7b53f26bdc1a)
![image](https://github.com/user-attachments/assets/051c7c4e-87d2-48b9-85c7-0e8ab0548fc9)
![image](https://github.com/user-attachments/assets/17081386-dc45-4382-a67f-c4c4617be971)
![image](https://github.com/user-attachments/assets/80749c2e-9cb5-4295-bd20-096058d34185)

5. Membuat Database Seeder
Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul
login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat
database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:
![image](https://github.com/user-attachments/assets/ed4bb94c-cf4b-4814-8dd8-6b71281f5149)

6. Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori
/app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut:
![image](https://github.com/user-attachments/assets/d2621563-64b9-4bfc-98a1-070c03cbe6f5)

7. Selanjutnya buka kembali CLI dan ketik perintah berikut:
![image](https://github.com/user-attachments/assets/71e30440-daf0-41e5-a6ef-e67f86a16b47)

8. Uji Coba Login
Selanjutnya buka url http://localhost:8080/user/login seperti berikut:
![image](https://github.com/user-attachments/assets/aa033f48-247e-4eea-9b28-68c239e2c595)

9. Menambahkan Auth Filter
Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php pada
direktori app/Filters.
 ![image](https://github.com/user-attachments/assets/978980e0-29ab-4c4d-822a-da66edcc8769)

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:
![image](https://github.com/user-attachments/assets/4bb197b7-33c5-48a5-a1de-a80d71e96bfd)

10. Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.
![image](https://github.com/user-attachments/assets/99f74673-662f-4603-ad58-daf2dcf3041d)

refresh kembali maka akan ke menu login

11. Fungsi Logout
Tambahkan method logout pada Controller User seperti berikut:
![image](https://github.com/user-attachments/assets/f9feadfc-55d8-45c3-b577-d271d20f2e5c)

pertemuan 5

1. Membuat Pagination
Pagination merupakan proses yang digunakan untuk membatasi tampilan yang panjang
dari data yang banyak pada sebuah website. Fungsi pagination adalah memecah tampilan
menjadi beberapa halaman tergantung banyaknya data yang akan ditampilkan pada
setiap halaman.
Pada Codeigniter 4, fungsi pagination sudah tersedia pada Library sehingga cukup mudah
menggunakannya.
Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi kode
pada method admin_index seperti berikut.
![image](https://github.com/user-attachments/assets/8a847c0a-d825-4a72-8214-753d4f86cb47)

2. Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut
dibawah deklarasi tabel data.
![image](https://github.com/user-attachments/assets/68b94114-b716-4fa9-beb7-70a5a792a152)
Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat
hasilnya.
![image](https://github.com/user-attachments/assets/c757b864-0bef-4a7e-8c5c-026a0f8fdd03)

3. Membuat Pencarian
Pencarian data digunakan untuk memfilter data.
Untuk membuat pencarian data, buka kembali Controller Artikel, pada method
admin_index ubah kodenya seperti berikut
![image](https://github.com/user-attachments/assets/5a9941cb-660c-4e0e-b71f-a4c3d74ca30a)

4. Kemudian buka kembali file views/artikel/admin_index.php dan tambahkan form
pencarian sebelum deklarasi tabel seperti berikut:
![image](https://github.com/user-attachments/assets/f7c958da-ad7a-45b5-8a44-9dcbd2247e38)
Dan pada link pager ubah seperti berikut.
![image](https://github.com/user-attachments/assets/74f3be13-71ab-495f-b04e-e1208ea14806)

5. Selanjutnya ujicoba dengan membuka kembali halaman admin artikel, masukkan kata
kunci tertentu pada form pencarian.
![image](https://github.com/user-attachments/assets/9d41ee1f-14c9-4abc-a5c6-e7b31dfaa412)

pertemuan 6

1. Upload Gambar pada Artikel
Menambahkan fungsi unggah gambar pada tambah artikel.
Buka kembali Controller Artikel pada project sebelumnya, sesuaikan kode pada method
add seperti berikut:
![image](https://github.com/user-attachments/assets/21bc13bb-ca15-401a-95cb-f36b98424940)

2. Kemudian pada file views/artikel/form_add.php tambahkan field input file seperti
berikut.
![image](https://github.com/user-attachments/assets/9354d4ed-f97f-4778-8510-ffb64d6b9422)
Dan sesuaikan tag form dengan menambahkan ecrypt type seperti berikut.
![image](https://github.com/user-attachments/assets/8ab19c09-fc41-4f4e-aa50-2de8d3d2fd66)

3. Ujicoba file upload dengan mengakses menu tambah artikel.
![image](https://github.com/user-attachments/assets/2e991a3d-2e26-44f8-8fbb-00ac9fc2ed22)
